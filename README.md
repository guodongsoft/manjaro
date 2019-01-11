# Manjaro initialize and config #

## Initialize ##

### fcitx ###

``` fish

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

