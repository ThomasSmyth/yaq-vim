# yaq-vim

_vim Syntax Highlighting and Indenting Support for k and q/kdb+_

Yet another vim syntax highlighting for kdb+, forked from
[vim-qkdb-syntax](https://github.com/katusk/vim-qkdb-syntax) by
[katusk](https://github.com/katusk), which is derived from
[vim](https://github.com/simongarland/vim) by
[Simon Garland](https://github.com/simongarland).
There is additional inspiration from [qvim](https://github.com/patmok/qvim) by
[patmok](https://github.com/patmok).

This repo adds special highlighting for:
- Query keywords, `select`, `update`, `upsert`, `insert`, `exec`, `delete`,
 `by` and `from`.
- Most keywords up to kdb+ v4.0 2022.09.30.

## Installation
This guide assumes your vim configuration files are located within
your home directory.

Ensure syntax highlighting is enabled in `~/.vimrc`.
```
syntax on
```

Copy the `\*.vim` files from [`syntax`](syntax) and [`indent`](indent)
to their corresponding directories under `~/.vim/`, creating them if need be.

If it does not exist then copy [`filetype.vim`](filetype.vim) to `~/.vim/`.
If [`filetype.vim`](filetype.vim) already exists then just insert the
relevant k & q lines from this repo.

Most of the work is done in [`k.vim`](syntax/k.vim) (which is loaded into 
[`q.vim`](syntax/q.vim)) as q "only" adds the functions in `.q` as
primitives, and relaxes the restriction on underscores in names.
