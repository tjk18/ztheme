# ztheme
A small and fast theme engine for zsh.

## How to install
### On Arch Linux (this way, you can use `pacman -R` to uninstall and you don't have to manually uninstall it to update):
```
git clone https://github.com/SkyyySi/ztheme-git
cd ztheme-git
makepkg -sifc
```
### On other distros:
```
git clone https://github.com/SkyyySi/ztheme
cd ztheme
sudo make install
```

Additionally, you have to add the following to your ~/.zshrc file (or /etc/zsh/zshrc to enable for all users) in order to activate ztheme:
```
if [ -f "/usr/share/ztheme/plugins/ztheme.plugin.zsh" ];then
	source "/usr/share/ztheme/plugins/ztheme.plugin.zsh"
fi
```

## How to use
To change the theme, simply type `ztheme prompt <theme name>` into a terminal (for example: `ztheme prompt agnoster` ). Your theme will be applied imediatly and it will be restored when you open a new terminal.
Similarly, you can turn plugins on and off by typing `ztheme plugin on <plugin name>` and `ztheme plugin off <plugin name>` respectively.

## How to add your own themes
You can add them either into the user directory at `$ZTHEME_USER_THEME_DIR/themes/` (set when ztheme is loaded, defaults to `~/.zsh/themes/` ), or if you want them to be usable by every user, you can put them into `$ZTHEME_SYSTEM_THEME_DIR/themes/` .

### Notes:
- If you don't set a valid theme, you will get an error. However, no default themes is set by default, so if you get an error message (after installing and opening a new terminal), don't worry. Just type `ztheme prompt classic` and it will go away.
- Some themes are modified versions of other peoples themes, all rights belong to them (the ones I reused have credits writtin at their to).
- This is a very new project, bugs are to be expected (although it works pretty much flawlessly for me).
