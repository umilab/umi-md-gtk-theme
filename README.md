# UMI ArcX Theme

UMI ArcX a flat theme with transparent elements, base on Arc theme with "X" picked design, for GTK 3, GTK 2 and GNOME Shell which supports GTK 3 and GTK 2 based desktop environments like GNOME, Unity, Budgie, Pantheon, Xfce, MATE, etc.

## UMI ArcX is available in three variants 

##### UMI-arcx

![A screenshot of the UMI ArcX theme](http://i.imgur.com/Ph5ObOa.png)

##### UMI-arcx-darker

![A screenshot of the UMI ArcX-Darker theme](http://i.imgur.com/NC6dqyl.png)

##### UMI-arcx-Dark

![A screenshot of the UMI ArcX-Dark theme](http://i.imgur.com/5AGlCnA.png)

## Installation

### Manual Installation

To build the theme the following packages are required
* `autoconf`
* `automake`
* `sassc` for GTK 3, Cinnamon, or GNOME Shell
* `pkg-config` or `pkgconfig` for Fedora
* `git` to clone the source directory
* `optipng` for GTK 2, GTK 3, or XFWM
* `inkscape` for GTK 2, GTK 3, or XFWM

The following packages are optionally required
* `gnome-shell`for auto-detecting the GNOME Shell version
* `libgtk-3-dev` for Debian based distros or `gtk3-devel` for RPM based distros, for auto-detecting the GTK3 version

**Note:** For distributions which don't ship separate development packages, just the GTK 3 package is needed instead of the `-dev` packages.

For the theme to function properly, install the following
* GNOME Shell 3.18 - 3.32, GTK 3.18 - 3.24
* The `gnome-themes-extra` package
* The murrine engine. This has different names depending on the distro.
  * `gtk-engine-murrine` (Arch Linux)
  * `gtk2-engines-murrine` (Debian, Ubuntu, elementary OS)
  * `gtk-murrine-engine` (Fedora)
  * `gtk2-engine-murrine` (openSUSE)
  * `gtk-engines-murrine` (Gentoo)

Install the theme with the following commands

#### 1. Get the source

Clone the git repository with

    git clone https://github.com/umilinux/umi-arcx-theme --depth 1 && cd arc-theme

#### 2. Build and install the theme

    ./autogen.sh --prefix=/usr
    sudo make install

Other options to pass to autogen.sh are

    --disable-transparency     disable transparency in the GTK3 theme
    --disable-light            disable UMI ArcX Light support
    --disable-darker           disable UMI ArcX Darker support
    --disable-dark             disable UMI ArcX Dark support
    --disable-cinnamon         disable Cinnamon support
    --disable-gnome-shell      disable GNOME Shell support
    --disable-gtk2             disable GTK2 support
    --disable-gtk3             disable GTK3 support
    --disable-metacity         disable Metacity support
    --disable-unity            disable Unity support
    --disable-xfwm             disable XFWM support
    --disable-plank                disable Plank theme support
    --disable-openbox              disable Openbox support

    --with-gnome-shell=<version>   build the gnome-shell theme for a specific version
    --with-gnome=<version>     build the theme for a specific GNOME version (3.14, 3.16, 3.18, 3.20, 3.22)
                               Note 1: Normally the correct version is detected automatically and this
                               option should not be needed.
                               Note 2: For GNOME 3.24, use --with-gnome-version=3.22
                               (this works for now, the build system will be improved in the future)

After the installation is complete the theme can be activated with `gnome-tweak-tool` or a similar program by selecting `UMI-ArcX`, `UMI-ArcX-Darker` or `UMI-ArcX-Dark` as Window/GTK+ theme and `UMI-ArcX` or `UMI-ArcX-Dark` as GNOME Shell/Cinnamon theme.

If the `--disable-transparency` option was used, the theme will be installed as `UMI-ArcX-solid`, `UMI-ArcX-Darker-solid` and `UMI-ArcX-Dark-solid`.

## Uninstall

Run

    sudo make uninstall

from the cloned git repository, or

    sudo rm -rf /usr/share/themes/{UMI-ArcX,UMI-ArcX-Darker,UMI-ArcX-Dark}

## Extras

### UMI ArcX KDE
A port of UMI ArcX for the Plasma 5 desktop with a few additions and extras. Available [here](https://github.com/PapirusDevelopmentTeam/arc-kde).

### Arc icon theme
The Arc icon theme is available at https://github.com/NicoHood/arc-icon-theme

### Plank theme
As of version `20180114` the plank theme will be installed along with the normal arc gtk theme. You can disable the install by passing `disable-plank` to the autogen command.
Now open the Plank preferences window by executing `plank --preferences` from a terminal and select `Gtk+` as the theme.

### FirefoxColor theme
Arc color palettes for FirefoxColor testpilot project

1.[Arc](https://color.firefox.com/?theme=XQAAAALsAAAAAAAAAABBqYhm849SCiazH1KEGccwS-xNVAWBveAusLC2VAlvlSjJ6UJSeqAgCYbdusEoPO6gs3O7v6uHbeft01vfMj--IcmWccV5ZVhbS5pAY21H4rQoo83UfS5UcAgLsFRnmMUloj0SFmW1HehCUMDfDxPPF1kUuA9qWMRgNi28lIsiXLMPZZcTMJdrmyjo335zNimxUcokvCK-KCKaas3H1WasbB4OVMJidW2cC2pVrAp_-pQmAA)

2.[Arc-Dark](https://color.firefox.com/?theme=XQAAAALsAAAAAAAAAABBqYhm849SCiazH1KEGccwS-xNVAVYwOBtiY0uPWyYE7WQD-5SgdZ71r2F-lXEQxrGAEzv_buK8bCyok70SsUy0GeciWa6veHgAFpeOvR5esr0TgHrmzAVtbaluSV2pYGKFkF03u_F69WpX-5y0OWddI2Y12nn6XZrfhTCe6wjAGRgrpfgKzbG8oTgp9v362NBpHcLnPzzzzC_3PGq4PfhQJimy-2PSgzHFoG6322X_-hAUAA)

3.[Arc-Darker](https://color.firefox.com/?theme=XQAAAALsAAAAAAAAAABBqYhm849SCiazH1KEGccwS-xNVAWBveAusLC2VAlvlSjJ6UJSeqAgCYbdusEoPO6gs3O7v6uHbeft01vfMkT1y4Tf1nzX1xYaRp0u6XBPage606lAwQt0F0O7Q6pf8R-lAjw8ljDMgG2fgvNk2K-ZUhapxWWNnKLb0LTrm1yLUWJYMgTx2cr9o4MWazvWLg9DPQcdumiH0qiUFROpAtIMassKweMS9iAEenpp0qT_Et_AAA)

### Arc-Dark for Ubuntu Software Center
The Arc Dark theme for the Ubuntu Software Center by [mervick](https://github.com/mervick) can be installed from [here](https://github.com/mervick/arc-dark-software-center). It solves readability issues with Arc Dark and the Ubuntu Software Center.

## Troubleshooting

If you get artifacts like black or invisible backgrounds under Unity, disable overlay scrollbars with

    gsettings set com.canonical.desktop.interface scrollbar-mode normal


## Bugs
If you find a bug, please report it at https://github.com/umilinux/umi-arcx-theme/issues

## License
UMI ArcX is available under the terms of the GPL-3.0. See `COPYING` for details.

## Full Preview
![A full screenshot of the Arc theme](http://i.imgur.com/tD1OBQ3.png)
<sub>Screenshot Details: Icons: [Arc](https://github.com/umilinux/umi-arcx-theme) | Launcher Icons based on [White Pixel Icons](http://darkdawg.deviantart.com/art/White-Pixel-Icons-252310560) | [Wallpaper](https://pixabay.com/photo-869593/) | Font: Futura Bk bt</sub>
