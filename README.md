## Vim Syntax Highlighting and Indenting Support for k and q/kdb+

This repository contains slightly modified variants of the [syntax highlighting files of Simon Garland](http://code.kx.com/wsvn/code/contrib/simon/vim/) for the k and q/kdb+ programming languages. All credits go to the original author, Simon Garland. There are other variants, namely:

- [bitbucket.org/alexcolson/kdb-vim.git](https://bitbucket.org/alexcolson/kdb-vim.git)
- [github.com/patmok/qvim](https://github.com/patmok/qvim)

_Why another variant?_ I did not like the highlight link to-group target colors in the original one, especially with the solarized-dark color scheme.

For example, I almost exclusively use `//` to begin line comments in q, not with any particular special meaning or emphasis, just to keep compatibility with other editors' C-like syntax highlighting schemes lacking syntax highlighting for q. Originally, target color for the `kSpecialComment` group covering line comments starting with `//` was `SpecialComment`, which translates to a strong red color in case of solarized-dark. Now it is simply `Comment`, which is the expected-by-me neutral grey color. See the `hi link` commands for all the minor target-group tweaks.

_Installation without a plugin manager._ The following is an excerpt from the original `readme.txt` by Simon Garland.

> Copy the files [...] to your vim home directory (probably `$HOME/.vim`).
> 
> If you already have a `filetype.vim` then just insert the additional k and q lines.
> 
> Copy the `*.vim` files from `<syntax>` and `<indent>` to their corresponding directories, creating them if need be.
> 
> Most of the work is done in `k.vim` (which is loaded into `q.vim`) as q "only" adds the functions in `<.q>` as primitives, and relaxes the restriction on underscores in names.

_Syntax highlighting in action._ The following screenshot shows the q.k file opened in vim with k syntax highlighting enabled, using the [solarized-dark](http://ethanschoonover.com/solarized) color scheme.

![k syntax highlighting](https://raw.githubusercontent.com/katusk/vim-qkdb-syntax/master/img/vim_qk_syntax_solarized_dark.png)
