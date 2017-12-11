# netrw Basics

I tried out NERDTree and I just didn't like it. I'm not sure exactly why. I guess it just seemed too clanky for me, it had too many features that I didn't care to learn. netrw is the default file explorer in [neovim](https://neovim.io/doc/user/pi_netrw.html#g:netrw_liststyle) and [vim](http://vimdoc.sourceforge.net/htmldoc/pi_netrw.html). 

Ultimately, I ended up coming across a few blog posts that led me to invest more time learning about netrw: [Vim: you don't need NERDtree or (maybe) netrw](https://shapeshed.com/vim-netrw/) and [The Power of Vim Plugins: netrw](http://snow-dev.com/the-power-of-vim-plugins-netrw/)

The following encompasses the settings and keymappings that I find useful as a starting point. In the future, I'll explore some more advanced features of netrw.


## Usage

### Open netrw

+ `:e <directory>` :  Open any directory in netrw
+ `:Sexplere` :  Open netrw in a horizontal split (-)
+ `:Vexplore` :  Open netrw in a vertical split (|)
+ `:Explore` :  Open netrw in the current window

### Open a file in netrw

+ ENTER :  in current window 
+ o :  open with horizontal split
+ v :  open with vertical split
+ p :  open preview of file in horizontal view
+ P :  open in previous used window
+ ctrl-^ (ctrl-shift-6) :  Returns to the last edited buffer.


## My init.vim Setup

```nvim
let g:netrw_banner = 0 " disable the banner 
let g:netrw_liststyle = 3
let g:netrw_browse_split = 0
let g:netrw_winsize = 20 " set the horizontal split width (percent)
```

### g:netrw_liststyle 

+ 0 :  one file per line
+ 1 :  one file per line with timestamp and size
+ 2 :  multiple files in columns
+ 3 :  tree style listing (you probably want this, I'm not sure why you'd even use the other ones, try them out by clicking i in netrw and see for yourself)

### netrw_browse_split

+ 0 :  open file in current window
+ 1 :  open file in horizontal split
+ 2 :  open file in vertical split
+ 3 :  open file in new tab
+ 4 :  open file in previous window


## Extras

### Open the drawer when you open a file*
```nvim
augroup ProjectDrawer
  autocmd!
  autocmd VimEnter * :Vexplore
augroup END
```

# TODO:

+ [vim-vinegar](https://github.com/tpope/vim-vinegar)
+ [CtrlP](https://github.com/kien/ctrlp.vim)
