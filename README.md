# Android-x86 Linux Surface Firmware

Android-x86 and Linux running on the Microsoft Surface devices. With this installtion method there is no need to recompile Kernel or initrd.img. 
This is key for Android-x86 and Kali-Linux operating systems with Kernels that can't be configured to their original state. This installation
uses /etc/init.d script to load modules before boot. The way the Linux kernel is configured with the firmware it has a file named config.bin 
in each directory so it will conflict with different Surface models this is why it is device specific zip files.

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

### Requirements

* For Linux udev is a dependency.

### Installation Instructions

1. Go to your devices folder after you extract zip file and open terminal.

2. Run the command sudo su for Linux then run this command cp -r * /
* next chmod 755 /etc/init.d/surface_mod

3. For Android use Termux run su and then cp -r etc /system
* next chomd 755 /system/etc/firmware/
* last chmod 755 /system/etc/init.d/surface_mod

4. Surface Go only touchscreen config:

* For touchscreen configration for Surface Go you need to run in a Linux environment Termux may work for Android after running su however the output file for the Linux environment can be copied and installed to the same directory for Android in the system.img 
* the commands below are to be run post install they are Linux and Android specific.

* Linux:

sudo su
echo "echo \"on\" > /sys/devices/pci0000:00/0000:00:15.1/i2c_designware.1/power/control" > /etc/init.d/surfacego-touchscreen
chmod 755 /etc/init.d/surfacego-touchscreen
update-rc.d surfacego-touchscreen defaults

* Android: Termux:

su
echo "echo \"on\" > /sys/devices/pci0000:00/0000:00:15.1/i2c_designware.1/power/control" > /system/etc/init.d/surfacego-touchscreen
chmod 755 /system/etc/init.d/surfacego-touchscreen

5. Then run command reboot and your firmware will be loaded next boot.




Best regards
Ryan Johnson




