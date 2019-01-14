# Manjaro initialize and config #

## Initialize ##

### archlinuxcn ###

``` fish
$ sudo vim /etc/pacman.conf # 打开文件
# 在文件末尾添加以下两行
[archlinuxcn]
Server = https://mirrors.ustc.edu.cn/archlinuxcn/$arch

$ sudo pacman -Syyu && sudo pacman -S archlinuxcn-keyring

```

### yay ###

``` fish
$ sudo pacman -S yay

```

### fcitx ###

``` fish
$ yay -S fcitx-im # 安装fcitx 选择全部安装
$ yay -S fcitx-configtool # fcitx 配置界面

安装fcitx-googlepinyin和fcitx-mozc

$ sudo vim ~/.xprofile # 打开编辑.xprofile文件
# 在文件中加入以下两行代码
export GTK_IM_MODULE=fcitx
export QT_IM_MODULE=fcitx
export XMODIFIERS="@im=fcitx"
```

### polybar ###

``` fish
$ yay -S polybar
```

### shutter ###

``` fish
$ yay -S shutter
```

### wps ###

``` fish
$ yay -S wps-office     # 安装wps
$ yay -S ttf-wps-fonts  # 安装wps字体

$ sudo vim /usr/bin/wps     # 编辑wps配置文件
# 在 紧跟#!/bin/bash后添加下列三行
export GTK_IM_MODULE=fcitx
export QT_IM_MODULE=fcitx
export XMODIFIERS="@im=fcitx"
```

## Config ##

### dmenurc ###

``` fish
rm ~/.dmenurc OR mv ~/.dmenurc ~/.dmenurc.bak
ln -s ~/.config/manjaro/dmenurc ~/.dmenurc
```

### Xresources ###

``` fish
rm ~/.Xresources OR mv ~/.Xresources ~/.Xresources.bak
ln -s ~/.config/manjaro/Xresources ~/.Xresources
ln -s ~/.config/manjaro/extend.Xresources ~/.extend.Xresources

```

### compton ###

``` fish
rm ~/.config/compton.conf OR ~/.config/compton.conf.bak
ln -s ~/.config/manjaro/compton.conf ~/.config/compton.conf
```

### i3 ###

``` fish
rm ~/.i3/config OR mv ~/.i3/config ~/.i3/config.bak
ln -s ~/.config/manjaro/i3/config ~/.i3/config
```

### polybar ###

``` fish
cd ~/.config
rm -rf polybar OR mv polybar polybar.bak
ln -s ~/.config/manjaro/polybar ~/.config/polybar
```

