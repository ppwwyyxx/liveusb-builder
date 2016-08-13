# liveusb-builder
A script suite to create multiboot USB stick for GNU/Linux distributions

## dependencies

- udevil: for mounting iso files  
- wget: for downloading
- GRUB with BIOS and UEFI support

## usage

First mount your USB drive partition. I recommend using udevil so that you can write files without as root.

Then run buildlive script as follows, suppose your USB is /dev/sdb and /dev/sdb1 is mount to /media/sdb1:

```
# install Arch, Mint (x86_64 with MATE Desktop) and Fedora to USB
./buildlive --root=/media/sdb1 --dev=/dev/sdb arch mint/64/mate fedora
```

## status

The resulting USB stick works on QEMU with PC BIOS (SeaBIOS), UEFI (OVMF), libreboot (i440fx, GRUB txtmode) as firmware.

## Related work

You can search keyword ``multiboot`` on GitHub and find some related projects. Listed below is some related work I know or find.

- [Yumi](http://www.pendrivelinux.com/yumi-multiboot-usb-creator/)  
- [MultiBootLiveUSB](https://github.com/moontide/MultiBootLiveUSB)
- [Multiboot USB drive - ArchWiki](https://wiki.archlinux.org/index.php/Multiboot_USB_drive)
- [cbodden/multiboot](https://github.com/cbodden/multiboot)
- [mbusb/multibootusb](https://github.com/mbusb/multibootusb)

