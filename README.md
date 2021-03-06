# Gamestarter Pi
![Gamestarter-logo](https://github.com/bite-your-idols/gamestarter/raw/master/assets/gamestarter-logo-dark.jpg)

English/[Spanish](https://github.com/bite-your-idols/gamestarter/blob/master/README-ES.md)


## Retrogamig addon for Raspberry Pi's Kodi.

If you use a Raspberry Pi as a media center running Kodi on [LibreELEC](https://libreelec.tv/) or [OpenELEC](http://openelec.tv/), you like retrogaming and you want to launch games just as you do with movies and tv shows without dual-booting, swaping SD memories, complex installations... Here you have the definitve solution.

With this addon you will continue with your own customized Kodi but empowered including: 
- Retroarch multi-emulator frontend with joypad configs,
- AdvancedLauncher addon with default emulators list and a custom skin,
- Emulationstation frontend,
- Amiga UAE4ARM emulator included in AdvancedLauncher and Emulationstation frontends,
- Some test freeware roms.

Also, you will have the choice of one-click installation of:
- Internet Archive ROM Launcher addon to launch games from the "cloud",
- 3 GameMaker Pi ports including modern masterpiece "Maldita Castilla".


## Installation Instructions
Download the latest release of the addon from [Releases Page](https://github.com/bite-your-idols/Gamestarter-Pi/releases/latest), copy into your Raspberry Pi and select "install from zip" in Settings>Addons menu. The first time the addon is launched it will perform some settings. Then copy your [roms and bios](https://github.com/libretro/Lakka/wiki/ROMs-and-BIOSes) to /storage/emulators/ folder via ftp or [samba](http://wiki.openelec.tv/index.php/Accessing_Samba_Shares) and reboot.

>Before installation you can backup your system or create an image of your SD card using [USB Image Tool](http://www.alexpage.de/usb-image-tool/).
>The addon has ben tested into OpenELEC 6, OpeneELEC 7 beta and LibreELEC 7 in a Raspberry Pi 2/3 model B and everything is working ok. I also recommend to read this whole text before installation to understand what is this all about.

![screenshot-addon](https://github.com/bite-your-idols/gamestarter/raw/master/assets/screenshot-gamestarter.png)


##### Addon Settings 
In addon settings you can define what frontend you want to use everytime you launch the addon, between RetroArch and EmulationStation.
From there, you can also install Internet Archive ROM launcher and GameMaker Pi ports. More options are coming...

![screenshot-addon-settings](https://github.com/bite-your-idols/gamestarter/raw/master/assets/screenshot-gamestarter-settings-2.png)



.


## Frontends

#### RetroArch:
The easiest and fastest way of retrogaming is using [Retroarch](http://www.libretro.com/). 
The first time RetroArch is launched I recommend to update (Settings menu> Online Updater) databases and download boxarts/thumbnails. Then you can create your own playlists, start games, change cores, user dynamic wallpapers... just like in [Lakka](http://www.lakka.tv/) distro!!

![screenshot-retroarch](https://github.com/bite-your-idols/gamestarter/raw/master/assets/screenshot-retroarch.gif)

.

#### AdvancedLauncher:

The most "Kodi-like" way to launch RetroArch games, amiga roms and GameMaker Pi ports, is using [AdvancedLauncher](https://github.com/edwtjo/advanced-launcher), located also under Program Addons. Using this you will get all your games just like your movies or music, integrated in Kodi.


![screenshot-advlauncher-context](https://github.com/bite-your-idols/gamestarter/raw/master/assets/screenshot-advlauncher-context.png)


There is a default/example launchers/games list I created. You can edit list, scan for your games, edit emulator cores... everything using contextual menu.


![screenshot-advlauncher-edit](https://github.com/bite-your-idols/gamestarter/raw/master/assets/screenshot-advlauncher-edit.png)


Also, there is a "Frontend" category where you can launch both RetroArch and EmulationStation.
![screenshot-advlauncher-frontends](https://github.com/bite-your-idols/gamestarter/raw/master/assets/screenshot-advlauncher-frontends.png)

.

#### EmulationStation:
Finally, [EmulationStation](https://github.com/Herdinger/EmulationStation) frontend is included.
You can customize system lists editing /storage/.config/emulationstation/es_systems.cfg file
![screenshot-emulationstation](https://github.com/bite-your-idols/gamestarter/raw/master/assets/screenshot-emulationstation.png)

.


> This frontend does not work in OE6-.

.

## Bonus

#### Amiga emulation:

Amiga Emulation is a little tricky and you can choose between uae4arm-libretro experiemntal core and  [UAE4ARM Pi](https://www.raspberrypi.org/forums/viewtopic.php?t=110488) port. You can not launch emulator into GUI by now, but you can launch games from Kodi's Advanced Launcher or Emulationstation. Games must be ".adf" files. All files from Multi-disk games must be named the same adding "_Disk1.adf", "_Disk2.adf"... like this:

> name of the game_Disk1.adf

> name of the game_Disk2.adf

> name of the game_Disk3.adf

> ...

With non libretro emulator you will need a mouse in order to start games and a keyboard to exit, save/load states...


.


#### GameMaker Pi:
As an extra feature, there is an optional installation of three free games from [GameMaker Team](http://yoyogames.com/pi). To make them work I had to make a [hacklib](http://forum.kodi.tv/showthread.php?pid=1481392#pid1481392) in order to downgrade some OpenELEC libs. If you notice that this downgrade is making some curl-related issues to your system, you can toggle the hack on/off using an addon I created and installed under Program addons menu called "hacklib".

![screenshot-gamemaker](https://github.com/bite-your-idols/gamestarter/raw/master/assets/screenshot-gamemaker.png)

You can exit them using ssh too:
```
pkill MalditaCastilla
pkill SuperCrateBox
pkill TheyNeedToBeFed
```

> These games only work with Xbox Controller :(

> These games have sound issues in OE7+.

.



#### Internet Archive ROM Launcher:

Finally, after installing from Addon settings, you can use Video Addons > IARL addon, it will launch Games hosted on the Internet Archive. 

![screenshot-iarl](https://github.com/bite-your-idols/gamestarter/raw/master/assets/screenshot-iarl.jpg)

More info: [IARL](https://github.com/zach-morris/plugin.program.iarl/wiki)


.



## Support
- [OpenELEC Forums](http://openelec.tv/forum/128-addons/80244-gamestarter-easy-retrogaming-installation-script)
- [LibreELEC Forums](https://forum.libreelec.tv/thread-287.html)
- [Kodi Forums](http://forum.kodi.tv/showthread.php?tid=276002)
- [Raspberri Pi Forums - English](https://www.raspberrypi.org/forums/viewtopic.php?f=78&t=141847)
- [Raspberri Pi Forums - Spanish](https://www.raspberrypi.org/forums/viewtopic.php?f=76&t=142248)
- [Github Issues](https://github.com/bite-your-idols/Gamestarter-Pi/issues)


.

## Credits

- Original RetroArch addon by [Mezo](http://openelec.tv/forum/128-addons/72972-retroarch-addon-arm-rpi)

- RetroArch, UAE4ARM & EmulationStation compiled by [Escalade](http://openelec.tv/forum/124-raspberry-pi/80543-raspberry-pi2-3-openelec-7-0-kodi-16-0-retroarch)

- AdvancedLauncher "skin" images by [tronkyfran](https://github.com/HerbFargus/es-theme-tronkyfran)







