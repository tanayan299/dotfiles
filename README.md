# vimrc

## First
```
#yum install vim git vim-enhanced
```
clone this repository

1. to setup vimrc
```
cp dotfiles/vimfiles.tar $HOME
tar -xvf vimfiles.tar
```
2. to setup bashrc
```
cd dotfiles
cp -rf .config x86_64-unknown-linux-musl .bashrc $HOME
cd
source .bashrc
```

## Second
```
$ vim

:PlugClean
:PlugInstall
:PlugUpdate
```

## Install Powerline Fonts
```
git clone https://github.com/powerline/fonts
```
The installation script installs the fonts locally.
```
cd fonts
sh install.sh
```

