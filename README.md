Suru Icons & Cursors For Manjaro Linux
======================================

The purpose of this project is to alter the Suru icon theme for use with Manjaro Linux. The alterations included will be things such as colour modifications and Manjaro-specific icons.

## Copying or Reusing

This project has mixed licencing. You are free to copy, redistribute and/or modify aspects of this work under the terms of each licence accordingly (unless otherwise specified).

The Suru icon assets (any and all source `.svg` files or rendered `.png` files) are licenced under the terms of the [Creative Commons Attribution-ShareAlike 4.0 License](https://creativecommons.org/licenses/by-sa/4.0/).

Included scripts are free software licenced under the terms of the [GNU General Public License, version 3](https://www.gnu.org/licenses/gpl-3.0.txt).

## Installing & Using

Suru-Manjaro inherits icons from the Suru icon theme. This repository will be focusing on Manjaro-specific icons and modifications, so it is recommended that the Suru icon theme is installed.

```bash
# install Suru
sudo pacman -S suru-icon-theme-git
```

You can build and install Suru-Manjaro from source using Meson.

```bash
# build
meson "build" --prefix=/usr
# install
sudo ninja -C "build" install
```

By default it installs to `/usr/` but you can specify a different directory with a prefix like: `/usr/local` or `$HOME/.local`.

After which you should be able to pick Suru-Manjaro as your icon or cursor theme in GNOME Tweak tool, or you can set either from a terminal with:

```bash
# set the icon theme
gsettings set org.gnome.desktop.interface icon-theme "Suru-Manjaro"
# or the cursor theme
gsettings set org.gnome.desktop.interface cursor-theme "Suru-Manjaro"
```

### Uninstalling Suru-Manjaro

To uninstall Suru-Manjaro, simply run the following. (If you installed it without superuser priveleges just omit the  `sudo`.)

```bash
sudo ninja -C "build" uninstall
```

Once uninstalled you can reset your icon and cursor theme to the default setting by running the following.

```bash
# reset icon theme to default
gsettings reset org.gnome.desktop.interface icon-theme
# reset cursor theme to default
gsettings reset org.gnome.desktop.interface cursor-theme
```
## Contributing

Contributions are obviously welcome! If you would like to contribute to this project, please have [read this](/CONTRIBUTING.md) regarding contributions.

I personally have no intention from profiting from this project, so if you are interested in financially supportung Suru (and, by proxy, Suru-Manjaro), you can do so [here](https://snwh.org/donate).

## Credit

The FreeDesktop Suru icon set is designed & developed by:

 -- Sam Hewitt <sam@snwh.org>

The original Suru icon set and concept was created by:

 -- Matthieu James
 -- Canonical Design Team
