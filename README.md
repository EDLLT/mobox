> [!WARNING]
> This fork has been modified to not use Project IDs and Private tokens that download from gitlab unlike the original mobox.
>
> Instead, all the base packages, wine packages and
> the package manager itself are taken from [this repo](https://github.com/EDLLT/mobox_packages) by the installer script. The installer and the package-manager have also been modified to be more verbose
> about what they are doing in the background. UNLESS you use the non-wow64 version in which case it will default to using olegos2's gitlab project/token approach
>
> 
> The instructions, usage and everything else remains exactly the same.
> I had great ambitions for this project; however, I unfortunately don't have time and great alternatives to mobox exist.

# README
![logo](docs/img/logo.png "logo")

English
&nbsp;&nbsp;| &nbsp;&nbsp;
<a href="https://github.com/olegos2/mobox/blob/main/README-ru.md">Русский</a>
&nbsp;&nbsp;| &nbsp;&nbsp;
<a href="https://github.com/olegos2/mobox/blob/main/README-ua.md">Українська</a>
&nbsp;&nbsp;| &nbsp;&nbsp;
<a href="https://github.com/olegos2/mobox/blob/main/README-pt_BR.md">Português Brasileiro</a>
&nbsp;&nbsp;| &nbsp;&nbsp;
<a href="https://github.com/olegos2/mobox/blob/main/README-pl.md">Polski</a>
&nbsp;&nbsp;| &nbsp;&nbsp;
<a href="https://github.com/olegos2/mobox/blob/main/README-ja.md">日本語</a>
&nbsp;&nbsp;| &nbsp;&nbsp;
<a href="https://github.com/olegos2/mobox/blob/main/README-zh_CN.md">简体中文</a>
&nbsp;&nbsp;| &nbsp;&nbsp;
<a href="https://github.com/olegos2/mobox/blob/main/README-id.md">Bahasa Indonesia</a>

##

`Mobox` is a project designed to run windows x86 applications in [Termux](https://github.com/termux/termux-app) using [Box64](https://github.com/ptitSeb/box64) and [Wine](https://www.winehq.org/).

# Installation
1. Install
[Termux](https://f-droid.org/repo/com.termux_118.apk),
[Termux-X11](https://raw.githubusercontent.com/olegos2/mobox/main/components/termux-x11.apk) and
[Input Bridge](https://raw.githubusercontent.com/olegos2/mobox/main/components/inputbridge.apk).

2. Open termux and paste command

```bash
curl -o ~/x https://raw.githubusercontent.com/EDLLT/mobox/main/install && . ~/x
```

3. Type `mobox` in termux.

# Configuration
## Wine
Wine can be installed or uninstalled in `Manage packages` menu.
To select wine container, use option 4 in main menu.
Mesa VirGL, Turnip, Wine Mono and Gecko can be installed in Wine Start Menu.
## Settings
### Box86 and Box64 dynarec variables
There are two switchable menus to change dynarec variables in mobox settings menu.
For more information about dynarec variables see [Box64 usage](https://github.com/ptitSeb/box64/blob/main/docs/USAGE.md) and [Box86 usage](https://github.com/ptitSeb/box86/blob/master/docs/USAGE.md)
### System settings
To change wine locale, dxvk hud preset or Turnip settings, use `System settings` menu in mobox.
Fallback resolution is used only when x11 resolution couldn't be detected automatically.
If you have Snapdragon 8 Gen 1, 8+ Gen 1, 7+ Gen 2, enable the second option in `select a7xx flickering fix (TU_DEBUG)` in `System settings` menu.
### Root settings
If you have root, then you can use OOM Adjuster which is useful if low memory killer stops termux.
## Termux-X11 preferences
* `Display resolution mode` exact
* `Display resolution` 1280x720
* `Reseed Screen While Soft Keyboard is open` OFF
* `Fullscreen on device display` ON
* `Force Landscape orientation` ON
* `Hide display cutout` ON
* `Show additional keyboard` OFF
* `Prefer scancodes when possible` ON
## Controls
For touch controls Input Bridge app is required
## Uninstall
To uninstall mobox, use `Backup and restore` menu.
## Debugging
To enable logging - select option 2 in Mobox -> Settings -> Debug settings menu. Path to the log is /sdcard/mobox_log.txt

## Support status
### Android
* `Android 10` or higher is recommended.
### Device
* Most Android cellphones can run `mobox` and DirectX 9 games using Mesa VirGL.
* Snapdragon device with Adreno 6xx or Adreno 725-740 is recommended to achieve best performance and compatibility with Turnip+DXVK.
### Root
* Root is not required.

## Known issues
* If termux app crashes when trying to enter mobox menu, then remove custom theme scripts:
```bash
rm -rf $PREFIX/glibc/opt/termux-style
```
* Some devices may have prefix creation freeze issues when installing PhysX, in this case change settings in `Compatibility settings` menu
* For SD845 device, disable dri3 in `Compatibility settings` menu

## Support mobox
[boosty](https://boosty.to/olegos/donate)

#
Big thanks to Hugo, JeezDisReez, ptitSeb, MishkaKolos, Xanzo, Jotaros, Maxython and others for help.

[MishkaKolos Discord](https://discord.gg/ZAQnZzbCXq)


## Third party applications

[glibc-packages](https://github.com/termux-pacman/glibc-packages)

[Box64](https://github.com/ptitSeb/box64)

[Box86](https://github.com/ptitSeb/box86)

[DXVK](https://github.com/doitsujin/dxvk)

[DXVK-ASYNC](https://github.com/Sporif/dxvk-async)

[DXVK-GPLASYNC](https://gitlab.com/Ph42oN/dxvk-gplasync)

[VKD3D](https://github.com/lutris/vkd3d)

[D8VK](https://github.com/AlpyneDreams/d8vk)

[Termux-app](https://github.com/termux/termux-app)

[Termux-x11](https://github.com/termux/termux-x11)

[Wine](https://wiki.winehq.org/Licensing)

[wine-ge-custom](https://github.com/GloriousEggroll/wine-ge-custom)

[Mesa](https://docs.mesa3d.org/license.html)

[mesa-zink-11.06.22](https://github.com/alexvorxx/mesa-zink-11.06.22)

[Mesa-VirGL](https://github.com/alexvorxx/Mesa-VirGL)

