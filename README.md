# Android-x86 Linux Surface Firmware

Android-x86 and Linux running on the Microsoft Surface devices. With this installtion method there is no need to recompile Kernel or initrd.img. 
This is key for Android-x86 and Kali-Linux operating systems with Kernels that can't be configured to their original state. This installation
uses /etc/init.d script to load modules before boot. 

### Supported Devices

* Surface Book
* Surface Book 2
* Surface Go
* Surface Laptop
* Surface Laptop 2
* Surface Pro 3
* Surface Pro 4
* Surface Pro 2017
* Surface Pro 6
* Surface Studio

### What's Working

* Keyboard (and backlight)
* Touchpad
* 2D/3D Acceleration
* Touchscreen
* Pen
* WiFi
* Bluetooth
* Speakers
* Power Button
* Volume Buttons
* SD Card Reader
* Cameras 
* Hibernate
* Sensors (accelerometer, gyroscope, ambient light sensor)
* Battery Readings
* Docking/Undocking Tablet and Keyboard
* Surface Docks
* DisplayPort
* USB-C (including for HDMI Out)
* Dedicated Nvidia GPU (Surface Book 2)

### Instructions

1. Go to your devices folder after you extract zip file and open terminal.

2. Run the command su if you are Android or sudo for Linux then run this cp -r * /

3. Then run command reboot and your firmware will be loaded next boot.




Best regards
Ryan Johnson




