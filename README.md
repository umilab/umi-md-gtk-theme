# UMI ArcD Theme

UMI ArcD a flat theme with transparent elements, base on Arc theme with "D" picked design, for GTK 3, GTK 2 and GNOME Shell which supports GTK 3 and GTK 2 based desktop environments like GNOME, Unity, Budgie, Pantheon, Xfce, MATE, etc.

## UMI ArcD is available in three variants 

##### UMI-ArcD

![A screenshot of the UMI ArcD theme](http://tnga.github.io/sharedbazar/_assets/images/umi-mvx-dee-screenshot-20190511111010.png)

##### UMI-ArcD-Darker

![A screenshot of the UMI ArcD-Darker theme](http://tnga.github.io/sharedbazar/_assets/images/umi-mvx-dee-dr-screenshot-20190511111053.png)

##### UMI-ArcD-Dark

![A screenshot of the UMI ArcD-Dark theme](http://tnga.github.io/sharedbazar/_assets/images/umi-mvx-dee-d-screenshot-20190511110943.png)

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

    git clone https://github.com/umilinux/umi-arcd-theme --depth 1 && cd umi-arcd-theme

#### 2. Build and install the theme

    ./autogen.sh --prefix=/usr
    sudo make install

Other options to pass to autogen.sh are

    --disable-transparency     disable transparency in the GTK3 theme
    --disable-light            disable UMI ArcD Light support
    --disable-darker           disable UMI ArcD Darker support
    --disable-dark             disable UMI ArcD Dark support
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

After the installation is complete the theme can be activated with `gnome-tweak-tool` or a similar program by selecting `UMI-ArcD`, `UMI-ArcD-Darker` or `UMI-ArcD-Dark` as Window/GTK+ theme and `UMI-ArcD` or `UMI-ArcD-Dark` as GNOME Shell/Cinnamon theme.

If the `--disable-transparency` option was used, the theme will be installed as `UMI-ArcD-solid`, `UMI-ArcD-Darker-solid` and `UMI-ArcD-Dark-solid`.

## Uninstall

Run

    sudo make uninstall

from the cloned git repository, or

    sudo rm -rf /usr/share/themes/{UMI-ArcD,UMI-ArcD-Darker,UMI-ArcD-Dark}

## Extras

### UMI ArcD KDE
A port of UMI ArcD for the Plasma 5 desktop with a few additions and extras. Available [here](https://github.com/PapirusDevelopmentTeam/arc-kde).

### UMI MVX icon theme
The UMI ArcD icon theme is available at https://github.com/umilinux/umi-mvx-icons

### Plank theme
As of version `20180114` the plank theme will be installed along with the normal arc gtk theme. You can disable the install by passing `disable-plank` to the autogen command.
Now open the Plank preferences window by executing `plank --preferences` from a terminal and select `Gtk+` as the theme.

### FirefoxColor theme
Arc color palettes for FirefoxColor testpilot project

1.[Arc](https://color.firefox.com/?theme=XQAAAALsAAAAAAAAAABBqYhm849SCiazH1KEGccwS-xNVAWBveAusLC2VAlvlSjJ6UJSeqAgCYbdusEoPO6gs3O7v6uHbeft01vfMj--IcmWccV5ZVhbS5pAY21H4rQoo83UfS5UcAgLsFRnmMUloj0SFmW1HehCUMDfDxPPF1kUuA9qWMRgNi28lIsiXLMPZZcTMJdrmyjo335zNimxUcokvCK-KCKaas3H1WasbB4OVMJidW2cC2pVrAp_-pQmAA)

2.[Arc-Dark](https://color.firefox.com/?theme=XQAAAALsAAAAAAAAAABBqYhm849SCiazH1KEGccwS-xNVAVYwOBtiY0uPWyYE7WQD-5SgdZ71r2F-lXEQxrGAEzv_buK8bCyok70SsUy0GeciWa6veHgAFpeOvR5esr0TgHrmzAVtbaluSV2pYGKFkF03u_F69WpX-5y0OWddI2Y12nn6XZrfhTCe6wjAGRgrpfgKzbG8oTgp9v362NBpHcLnPzzzzC_3PGq4PfhQJimy-2PSgzHFoG6322X_-hAUAA)

3.[Arc-Darker](https://color.firefox.com/?theme=XQAAAALsAAAAAAAAAABBqYhm849SCiazH1KEGccwS-xNVAWBveAusLC2VAlvlSjJ6UJSeqAgCYbdusEoPO6gs3O7v6uHbeft01vfMkT1y4Tf1nzX1xYaRp0u6XBPage606lAwQt0F0O7Q6pf8R-lAjw8ljDMgG2fgvNk2K-ZUhapxWWNnKLb0LTrm1yLUWJYMgTx2cr9o4MWazvWLg9DPQcdumiH0qiUFROpAtIMassKweMS9iAEenpp0qT_Et_AAA)

## Troubleshooting

If you get artifacts like black or invisible backgrounds under Unity, disable overlay scrollbars with

    gsettings set com.canonical.desktop.interface scrollbar-mode normal

## Bugs
If you find a bug, please report it at https://github.com/umilinux/umi-arcd-theme/issues

## License
UMI ArcD is available under the terms of the GPL-3.0. See `COPYING` for details.

## Full Preview
![A full screenshot of the UMI ArcD theme](http://tnga.github.io/sharedbazar/_assets/images/umi-mvx-dee-lde-screenshot-20190511112245.png)
<sub>Screenshot Details: Icons: [UMI ArcD](https://github.com/umilinux/umi-mvx-icons) | [Wallpaper](https://wallpapers.cimiro.com/wp-content/uploads/sites/4/2019/01/background-beach-beautiful-207135-1.jpg) | Font: Futura Bk bt</sub>
