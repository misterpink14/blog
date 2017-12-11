# vim

Neovim is my flavor of vim and mac is my flavor of OS, so all posts are under that context. vim is also a fairly new thing for me, but I assume most of this applies to vim8 and beyond as well.

It's taken a really long time for me to be comfortable enough in vim make vim mode in IDEs (Intellij) and editors (VS Code) my go to. I'd really like for it to replace the need for test editors entirely for me and become my main editor (currently Intellij).   

Step 1: disable the arrow keys for navigation by adding this to your init.vim (in `~/.config/nvim`) file (.bashrc for vim users)

```nvim
noremap <Up> <NOP>
noremap <Down> <NOP>
noremap <Left> <NOP>
noremap <Right> <NOP>
```

# Posts
[netrw Basics](/blog/vim/netrw-basics)

