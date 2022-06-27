# My build of dmenu

My personal build of dmenu

## About
I use this repository as a way to version control any changes I make to my menu application.

## Patches done to dmenu
This build of dmenu is based on [dmenu 5.1](https://dl.suckless.org/tools/dmenu-5.1.tar.gz) (2022-02-11) and modified with patches and other changes to the sourcecode. I have kept all used *.diff files* to patch dmenu with in [master/patches](https://github.com/consoom/dmenu/tree/master/patches):

- [border](https://github.com/consoom/dmenu/blob/main/patches/dmenu-border-20201112-1a13d04.diff) ([source](https://tools.suckless.org/dmenu/patches/border/)) — allows dmenu prompt to have a border as option
- [center](https://github.com/consoom/dmenu/blob/main/patches/dmenu-center-20200111-8cd37e1.diff) ([source](https://tools.suckless.org/dmenu/patches/center/)) — allows dmenu prompt to be centered as option
- [mousesupport](https://github.com/consoom/dmenu/blob/main/patches/dmenu-mousesupport-5.1.diff) ([source](https://tools.suckless.org/dmenu/patches/mouse-support/)) — adds mouse support (scrolling, clicking, etc.)
- [password](https://github.com/consoom/dmenu/blob/main/patches/dmenu-password-5.0.diff) ([source](https://tools.suckless.org/dmenu/patches/password/)) — adds password input field to prompt as option
- [xresources](https://github.com/consoom/dmenu/blob/main/patches/dmenu-xresources-alt-5.0.diff) ([source](https://tools.suckless.org/dmenu/patches/xresources-alt/)) — reads colors and fonts from Xresources

## Installation
```
$ git clone https://github.com/consoom/dwm
$ cd dwm
$ sudo make clean install
```
**Important: you need to install `libxft-bgra` (available in the AUR on arch), otherwise dmenu will crash. This is caused by an issue in the normal libxft package that breaks rendering colored characters. [Read more](https://gitlab.freedesktop.org/xorg/lib/libxft/-/merge_requests/1).**

## Added options
- Password — usage: `dmenu -P`
- Border — usage: `dmenu -bw <pixels>`
- Center - usage: `dmenu -c`
