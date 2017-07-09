# operation-chromebook

### Hardware

  * HP Chromebook 11 G4 EE: Intel Celeron N2840 Dual Core, 11.6" Screen, 4GB RAM, 16GB Internal Storage. Bought for $210 CDN each at [Mike's Computer Shop](https://www.mikescomputershop.com/product/6961387).
    - 3x for kids: `echo`, `romeo`, `whiskey`
  * Lenovo Chromebook N42-20 80US0000US, Intel Celeron N3060, 14" Screen, 4GB RAM, 16GB Flash Memory Capacity. Bought for $190 CDN at [Mike's Computer Shop](https://www.mikescomputershop.com/product/7619358) (special price on a single machine that someone had returned).
    - 1x for me

### Links

  * <http://platypusplatypus.com/chromebooks/play-minecraft-chromebook/>
  * <https://github.com/dnschneid/crouton>
    * <https://github.com/dnschneid/crouton/wiki/crouton-in-a-Chromium-OS-window-%28xiwi%29>
  * <https://jwhollister.com/r/2017/04/14/chromebook-4-rstats.html>

### Live notes

Turn thing on. Sign in with each person's Google account and connect to the network.

Escape + Refresh + Power to reboot. You'll see recovery screen, do not panic. Ctrl + D to enable Developer mode. Yes, OK to wipe everything. Also, do not accept invitation to re-enable OS verification. Just wait that offer out or Ctrl + D to advance. Eventually you'll see "Preparing system for Developer Mode" for 7 - 8 mins. Another screen inviting you to re-enable OS verification. Wait it out or Ctrl + D.

Groundhog Day. Sign in to the Google accounts again and re-connect to the network.

Go to <https://github.com/dnschneid/crouton>. Click the repo's URL to download crouton.

*20/20 hindsight* The HPs somehow did not find the network smoothly enough to update themselves during the first (or second?) boot. At this point, in Chrome, go to `chrome://help` and accept the offer to update the OS and restart. Keep handling invitations to re-enable OS verification as above. This process looked slightly different on all of the HPs. Suspect they were actually not all of the same vintage?

Open a shell with Ctrl+Alt+T and enter `shell`. This will just be a tab in Chrome.

```sh
sudo sh ~/Downloads/crouton -t xfce
```

This took ~17 minutes. Pick a username and password for the Ubuntu side.

Convince self I've actually installed Ubuntu by staring an Xfce session:

```sh
sudo startxfce4
```

Looks good. Cycle between ChromeOS and the running chroot with Ctrl+Alt+Shift+Back and Ctrl+Alt+Shift+Forward. Note these are the arrows up with the function keys, not the ones in the lower left corner. To truly exit the chroot, log out of Xfce.

On Ubuntu, make sure everything up-to-date and install JRE:

```
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install default-jre
```

Install Minecraft. On the ChromeOS side, download the `.jar` by selecting linux from the [official download page](https://minecraft.net/en-us/download/).

Back to Ubuntu now.

```
mkdir games
mkdir games/minecraft
cp ~/Downloads/Minecraft.jar games/minecraft/
chmod a+x games/minecraft/Minecraft.jar
```

Launch it!

*OK, yeah, it didn't actually go quite this smoothly, but by the time I got to the 3rd Chromebook, I had worked out the above.*

<img src="img/minechrome_02.jpg" style="float: left; width: 30%; margin-right: 1%; margin-bottom: 0.5em;">
<img src="img/minechrome_03.jpg" style="float: left; width: 30%; margin-right: 1%; margin-bottom: 0.5em;">
<img src="img/minechrome_04.jpg" style="float: left; width: 30%; margin-right: 1%; margin-bottom: 0.5em;">
