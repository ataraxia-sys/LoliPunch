1) Install MrChromebox's UEFI drivers.
2) Install any Linux distribution of choice, so long as you have packages similar to `sof-firmware`, `kpartx`/`multipath-tools`, and `alsa-ucm-conf` installed.
3) Obtain the recovery image for your board family from https://cros.tech.
4) Unzip the image, leaving a `.bin` file in your directory.
5) Run this command: \
`sudo kpartx -av $BOARD.bin` \
assuming `$BOARD` is the beginning part of your .bin file.
6) Mount it with this command: \
`sudo mount -o ro /dev/mapper/loop0p3 /mnt`
7) Grab everything that isn't a symbolic link from `/mnt/lib/firmware` and `/mnt/usr/share/alsa/ucm`, and place it in the directory you will be running LoliPunch Installer from.
8) Feel free to audit LoliPunch Installer, it's open-source (unlike CoolStar's "driver" that he illegally sourced from some open source projects)!
9) Run LoliPunch Installer and follow directions. YOUR DEVICE WILL ASK FOR ROOT AND REBOOT, THIS IS NORMAL. \
GRAB SOME COFFEE AS WELL, THIS RECOMPILES YOUR KERNEL DUE TO KERNEL REGRESSIONS.
10) Enjoy your LoliPunch ;)
