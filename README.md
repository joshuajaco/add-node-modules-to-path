# add-node-modules-to-path

This fork only renamed the function to `add-node-modules-to-path`. For some reason it was not working under the original name ¯\\_(ツ)_/¯

This file provides `add-node-modules-to-path`, which searches
the current files parent directories for the `node_modules/.bin/` directory
and adds it to the buffer local `exec-path`.
This allows Emacs to find project based installs of e.g. eslint.

## Usage
`M-x add-node-modules-to-path`

To automatically run it when opening a new buffer:
(Choose depending on your favorite mode.)

```
(eval-after-load 'js-mode
  '(add-hook 'js-mode-hook #'add-node-modules-to-path))
```
