# Smart Home / OpenHAB

Get openHABian:
```
https://github.com/openhab/openhabian/releases
```

Write OpenHABian (or raspian) img to SD card (find you dev using e.g fdisk -l or df -h):
```
dd bs=4M if=2017-11-29-raspbian-stretch.img of=/dev/sdX status=progress conv=fsync
```

Boot and find your new host (default host name openhabian/raspberry)
```
nmap -sn 192.168.1.0/24
```

OpenHAB Secret and UUID:
```
/var/lib/openhab2/uuid
/var/lib/openhab2/openhabcloud/secret
```
