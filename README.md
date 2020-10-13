<p align="center"><a name="top" href="#envelope-overview"><img src="https://raw.githubusercontent.com/ComplexPlatform/KDE-dotfiles/master/.assets/header_.png"></a></p>

<h2 align="center"> Preview </h2>

![](https://raw.githubusercontent.com/ComplexPlatform/KDE-dotfiles/master/previews/foggy-mountain.png)

## :envelope: Overview

-  **OS:** Manjaro
-  **DE:** Plasma
-  **WM:** KWin
-  **Terminal:** Konsole
-  **Shell:** zsh + Oh My Zsh + Powerlevel10k
-  **Terminal Font:** SF Mono Powerline
-  **System Font:** SF UI Text
-  **Bar/Panel:** Latte-Dock
-  **File Manager:** ~~Dolphin~~ Thunar
-  **Editor:** VS Code
-  **Browser:** Firefox
-  **Music Player:** Spotify & ncmpcpp

The fetch shown in the preview above is [fet.sh](https://github.com/6gk/fet.sh)

Firefox CSS is based on [minimal-functional-fox](https://github.com/mut-ex/minimal-functional-fox)

Startpage source: https://notabug.org/nytly/home

Latte layout is based on [Moe Layout](https://store.kde.org/p/1373008/). Make sure to install the required widgets if you're going to use it.

ncmpcpp config is from [elenapan](https://github.com/elenapan/dotfiles/blob/master/config/ncmpcpp/config) and [owl4ce](https://github.com/owl4ce/dotfiles/blob/master/.ncmpcpp/config)

Materia GTK themes and Papirus icons are made using [oomox](https://github.com/themix-project/oomox)

## :pushpin: Important stuff

-  [Latte-Dock](https://github.com/KDE/latte-dock) & [Moe Layout](https://store.kde.org/p/1373008/)
-  [wpgtk](https://github.com/deviantfero/wpgtk) & [pywal](https://github.com/dylanaraps/pywal)
-  [qt5-styleplugins](https://github.com/qt/qtstyleplugins) ([AUR](https://aur.archlinux.org/packages/qt5-styleplugins/), can also be installed with `pacman`)
-  [CullaX](https://www.opendesktop.org/p/1278039/)

## :paperclip: Optional stuff

-  [Spicetify-cli](https://github.com/khanhas/spicetify-cli) (make sure to install [Dribbblish](https://github.com/morpheusthewhite/spicetify-themes/tree/master/Dribbblish) as well.)
- VS Code Extension - [Wal Theme](https://marketplace.visualstudio.com/items?itemName=dlasagno.wal-theme)
-  [Powerlevel10k](https://github.com/romkatv/powerlevel10k)
-  [Krohnkite](https://store.kde.org/p/1281790/)
-  [Zathura-Pywal](https://github.com/GideonWolfe/Zathura-Pywal)
-  [ncmpcpp](https://github.com/ncmpcpp/ncmpcpp)
-  [betterdiscordctl](https://github.com/bb010g/betterdiscordctl) & [pywal-discord](https://github.com/FilipLitwora/pywal-discord)

## :hammer_and_wrench: Setup

**(work in progress)**

If you know how to use `wpgtk`, just copy my templates and import the color scheme.

Note: I just got started ricing back in August so I'm very new to this. I don't guarantee anything to be working as intended.

1. Install the programs mentioned above.

2. For `wpgtk`, install the GTK template as instructed [here](https://github.com/deviantfero/wpgtk/wiki/Installation#default-templates) (skip this if you're going to use my GTK themes). For custom templates, follow the documentation. I have a template for `kdeglobals`, `Konsole`, and `CullaX`. You may copy the values but make sure to add them manually from the GUI, as the files use symbolic links.

	When you add a template, you will be asked to locate the specific file. Here's the location for each file if you're going to use my templates:

	+ `kdeglobals` - `~/.config/kdeglobals`
	+ `Konsole` - `~/.local/share/konsole/wpgtk.colorscheme` (copy the theme first from this repo)
	+ `CullaX` - `~/.local/share/plasma/desktoptheme/CullaX/colors`

3. For removing the title bar and adding active/inactive window frame colors, follow [this guide.](https://github.com/waltereikrem/KWin-TilingGuide/) (I recommend using `Krohnkite` for tiling.)
4. Launch `Latte-Dock`, import my layout, then apply.
5. Launch `wpgtk`. under Colors tab, click import and choose a `.json` file from [color schemes](https://github.com/ComplexPlatform/KDE-dotfiles/tree/master/color%20schemes). Under Wallpaper tab, click set.

	If you're using `Spicetify` with `Dribbblish` installed, copy [color.ini](https://github.com/ComplexPlatform/KDE-dotfiles/blob/master/.config/spicetify/Themes/Dribbblish/color.ini) from this repo to `~/.config/spicetify/Themes/Dribbblish/`. Replace when prompted.

	Afterwards, run the following:

	```
	spicetify config color_scheme pywal
	spicetify apply
	```

6. Go to System Settings. For Plasma Style, set it to CullaX. For Application Style, set it to gtk2. Click `Configure GNOME/GTK Application Style...`, set the GTK2 and GTK3 theme to FlatColor if you're using wpgtk's GTK template. For icons, just copy my custom Papirus icons to `~/.local/share/icons` and apply.

If wpgtk doesn't work for some reason, go to Options tab and make sure `pywal` is selected under `Select your backend:`. Click save. Then go to Wallpapes tab, add a random image, and click set after it fetches the colors. Import the color scheme again, click save, and then click set once again.
