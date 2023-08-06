# rpi_robot_v2
2 wheel diffdrive slam rpi robot

Udev rule
=
Following **REQUIRED** Udev rule is for automagically remapping ttyUSB* to ``ESP32`` and ``YDLIDAR``  
file named : [10-usb-for-ros2.rules](https://gist.github.com/TiNredmc/79490141916b39753ba583aa1a8f79b7)
```
SUBSYSTEM=="tty", ATTRS{idVendor}=="10c4", ATTRS{idProduct}=="ea60", SYMLINK+="YDLIDAR", MODE="0666"
SUBSYSTEM=="tty", ATTRS{idVendor}=="1a86", ATTRS{idProduct}=="7523", SYMLINK+="ESP32", MODE="0666"

```