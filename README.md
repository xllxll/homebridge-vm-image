# Homebridge VM Boot Image

A minimal ISO image that runs Homebridge. 

## Currently Experimental!

**For use in virtual machines only, do not boot this ISO in a machine with access to a disk containing data you care about.**

## Usage

1. Download the latest boot2homebridge.iso image here: https://github.com/oznu/boot2docker/releases
2. Create a new virtual machine in HyperV, VirtualBox, Parallels Desktop etc.
3. Configure your virtual machine with the following settings:
  * **RAM**: 1GB Minimum
  * **CPU**: 1+
  * **HDD**: 8GB virtual hard disk (thin / dynamic) 
  * **Network Adapter**: [Bridged Adapter](https://github.com/homebridge/homebridge/wiki/VirtualBox-and-Parallels-Desktop-VM-Network-Settings) (VirtualBox / Parallels Desktop) or External Switch (Hyper-V).
  * **ISO**: boot2homebridge.iso (this must stay attached forever, so store the .iso in a safe place).
    * VirtualBox: check the "Is Live CD" box.
    * Parallels Desktop: you may need to re-mount the ISO once after the first boot in the VM settings.
4. Start your VM.
5. Connect to the address shown in the console window, eg. `http://192.168.1.100:8581`.
6. Manage Homebridge.

<p align="center">
  <img src="https://user-images.githubusercontent.com/3979615/86241831-fb3a5e00-bbe6-11ea-8070-f3e6c2bf5ec6.png">
</p>

## Credits

Based on [boot2docker](https://github.com/boot2docker/boot2docker).