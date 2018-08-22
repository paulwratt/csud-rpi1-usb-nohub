# csud-rpi1-usb-nohub
boochow's patched csud for RPi A/A+/B/B+/Z/Z+W - direct, no hub

until the pull request is commited: https://github.com/Chadderz121/csud/pull/10

---

This makes it possible to connect a USB FS/LS device to the root hub directly (without USB HS hub).
It is useful if you want to connect a USB keyboard, for example, directly to the USB port of RPi model A/A+/Zero/Zero W because they have no on-board USB hub (LAN9512) and their USB port is the port of the root hub.
Patches included in this PR stops USB SSPLIT/CSPLIT packets when a USB device connected to the root hub is a FS or LS device. I also added some lines to hub.c for detecting unplugging a device from the root hub.
