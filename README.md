In this tutorial I show how to run Diablo 1 mod Tchernobog under Linux with wine setup.
=============================================

You will need:

* Wine installation on your modern Linux PC
* Winetricks installation
* DIABDAT.MPQ file from original Diablo game. You can buy Diablo on [GOG](https://www.gog.com/eng/game/diablo) or copy file from CD version.
* Tchernobog mod. Can be downloaded from official website [here](https://mod.diablo.noktis.pl/download).

Installation of Wine and Winetricks
---------------------------------------------
I don't write here about installation of Wine. Everything You can find depending on Your distro is on Wine website, [here on official wiki](https://gitlab.winehq.org/wine/wine/-/wikis/Download) and there's a plenty of tutorials on the internet.
From my experience I suggest to install development branch of Wine. That's it.

About Winetricks. Just install it from your packages repo. It will be outdated.
Run this command on terminal to make Winetricks updated to the latest version:
```
sudo winetricks --self-update
```

And here's the trick command
---------------------------------------------
This command will do the whole thing and make Tchernobog playable on Your PC with Wine.
Run it on terminal without sudo.
```
winetricks directmusic directplay dmband dmcompos dmime dmloader dmscript dmstyle dmsynth dmusic dmusic32 dsound dswave
```
This will install with winetricks nessesary libraries to make it work.

And finally Tchernobog mod
---------------------------------------------
Just download, unpack mod and copy DIABDAT.MPQ to main folder of mod.
Run exe with this command.
```
wine start /unix /home/<user>/Games/Tchernobog/Tchernobog.exe
```
Change path to proper one of Your folder where Tchernobog is.

Enjoy Your game!
