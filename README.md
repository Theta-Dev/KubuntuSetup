# KubuntuSetup

My Kubuntu setup. Used as a cheat sheet in case I have to set up my system again or on another PC.

Download Kubuntu: https://kubuntu.org/getkubuntu/

### Colors

ThetaDev / ThetaDev Dark color theme

![](assets/colors.png)

Copy the theme files into `~/.kde/share/apps/color-schemes/`

### Cursors

Copy `Win10Theta` cursor folder into `/usr/share/icons/`

### Filesystem

Currently I have my data on a seperate NTFS-formatted partition to allow access from Windows, too. Here is the fstab entry for it. Note that the `umask` (default file permissions) have to be set to that values, otherwise the trash can won't work (deleted files from the data partition will be copied to the system partition).

Get disk partition UUID: `blkid`

```
/etc/fstab
# DATEN
UUID=xxxxxxxxxxxxxxxx /media/Daten ntfs uid=1000,gid=1000,rw,user,exec,umask=0077 0 0
```

### KDE Settings

