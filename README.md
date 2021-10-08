# nvim-tmux-configuration

# Simple Setup

- vim: `8.2.3458`
- nvim: `0.4.4`

```bash
$ cp coc-settings.json init.vim ~/.vim 
$ cp .vimrc .tmux.conf ~
```

# Installation

## Prerequest 

```bash
$ sudo apt install ccls fzf tmux jq
```

`yarn` should be install

## Plugin Install

1. [vim plug](https://github.com/junegunn/vim-plug)

For Vim

```bash
$ curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

For Nvim

```bash
$ curl -fLo ~/.var/app/io.neovim.nvim/data/nvim/site/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

2. [coc](https://github.com/neoclide/coc.nvim)

Install nodejs

```bash
$ sudo apt install nodejs
$ sudo apt install openjdk-17-jdk openjdk-17-jre
```

Install esstential language server

```vim
:CocInstall coc-json coc-tsserver coc-ccls
```

My language server contains:
- coc-python
- coc-pyright
- coc-java
- coc-xml

## Usage

> Detailed operation is listed in `.vimrc` and `.tmux.conf`

For ROS dev

```bash
$ catkin build -DCMAKE_EXPORT_COMPILE_COMMANDS=1
$ jqros
```
