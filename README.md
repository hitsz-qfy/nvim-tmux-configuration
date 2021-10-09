# nvim-tmux-configuration

# Installation

## Prerequest 

- vim: `8.2.3458`

- nvim: `0.4.4`

- [ccls](https://github.com/MaskRay/ccls)

[build](https://github.com/MaskRay/ccls/wiki/Build), then [install](https://github.com/MaskRay/ccls/wiki/Install)

- [fzf](https://github.com/junegunn/fzf)

[Install](https://github.com/junegunn/fzf#installation)

- tmux 

```bash
$ sudo apt install tmux
```

- jq 

```bash
$ sudo apt install jq
```

- nodejs

```bash
$ sudo apt install nodejs
```

- openjdk

```bash
$ sudo apt install openjdk-17-jdk openjdk-17-jre
```

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

Install esstential language server

```vim
:CocInstall coc-json coc-tsserver coc-ccls
```

My language server also contains:
- coc-python
- coc-pyright
- coc-java
- coc-xml

# Simple Setup

```bash
$ cp coc-settings.json init.vim ~/.vim 
$ cp .vimrc .tmux.conf ~
```

# Usage

> Detailed operation is listed in `.vimrc` and `.tmux.conf`

For ROS dev

```bash
$ catkin build -DCMAKE_EXPORT_COMPILE_COMMANDS=1
```

Here you can find isolated `compile_commands.json` files under the directory of each ros package, then

```bash
$ jqros  # in the root of ros workspace
```

Then a `compile_commands.json` file concatenating json files from all ros packages is built.
