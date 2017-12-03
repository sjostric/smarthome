# Smart Home / OpenHAB

## Installation

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
ping openhabianpi.local
ssh openhabian@openhabianpi.local
passwd
``` 

Restarting OpenHAB:
```
sudo systemctl restart openhab2.service
```

For z-wave:
```
sudo vi /etc/default/openhab2
e.g:
EXTRA_JAVA_OPTS="-Dgnu.io.rxtx.SerialPorts=/dev/ttyUSB0:/dev/ttyS0:/dev/ttyS2:/dev/ttyACM0:/dev/ttyAMA0"

sudo raspi-config -> 5. Interface options -> Serial (disable for shell, enable hardware) 
```

OpenHAB Secret and UUID. First install the openhab cloud add-on (Paper UI -> Add-ons). You will need it create an online account or restore a previous cloud connection.
```
/var/lib/openhab2/uuid
/var/lib/openhab2/openhabcloud/secret
```
