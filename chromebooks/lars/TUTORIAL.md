1) Install MrChromebox's UEFI drivers.
2) If you have the C771-C4TM like me, ignore the fact that it says a different model in the setup screen.
3) Install any Linux distribution of choice, so long as you have packages similar to `sof-firmware`, `kpartx`/`multipath-tools`, and `alsa-ucm-conf` installed.
4) Obtain the recovery image for your board family from https://cros.tech.
5) Unzip the image, leaving a `.bin` file in your directory.
6) Run this command: \
`sudo kpartx -av $BOARD.bin` \
assuming `$BOARD` is the beginning part of your .bin file.
7) Mount it with this command: \
`sudo mount -o ro /dev/mapper/loop0p3 /mnt`
8) Grab everything that isn't a symbolic link from `/mnt/lib/firmware` and `/mnt/usr/share/alsa/ucm`, and place it in the directory you will be running LoliPunch Installer from.
9) Feel free to audit LoliPunch Installer, it's open-source (unlike CoolStar's "driver" that he illegally sourced from some open source projects)!
10) Run LoliPunch Installer and follow directions. YOUR DEVICE WILL ASK FOR ROOT AND REBOOT, THIS IS NORMAL.
11) Enjoy your LoliPunch ;)
