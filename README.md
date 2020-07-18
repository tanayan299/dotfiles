# vimrc

**WIP**

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

## bashrc
Installation of "powerline-go"
just installed Go, then installed powerline-go with go get.
```
$ sudo apt install golang-go
$ go get -u github.com/justjanne/powerline-go
```
Add this to ~/.bashrc.
```
GOPATH=$HOME/go
function _update_ps1() {
    PS1="$($GOPATH/bin/powerline-go -error $? \
        -modules jobs,exit,user,venv,cwd,perms,git,hg)"
}
if [ "$TERM" != "linux" ] && [ -f "$GOPATH/bin/powerline-go" ]; then
    PROMPT_COMMAND="_update_ps1; $PROMPT_COMMAND"
fi
```
Installation of "fzf"
```
git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
~/.fzf/install
```
