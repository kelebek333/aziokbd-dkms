# aziokbd-dkms
Linux Microdia Keyboard Chipset Driver

Original source => [Swoogan/aziokbd](https://bitbucket.org/Swoogan/aziokbd)

## Install Requirements

`sudo apt-get install build-essential git dkms linux-headers-$(uname -r)`

You must disable secureboot from BIOS/EFI settings

## How To Install

`git clone https://github.com/kelebek333/aziokbd-dkms`

`sudo dkms add ./aziokbd-dkms`

`sudo dkms build aziokbd/1.0.0`

`sudo dkms install aziokbd/1.0.0`

`sudo cp ./aziokbd-dkms/usbhid.conf /etc/modprobe.d`

## How To Remove

`sudo dkms remove aziokbd/1.0.0 --all`

`sudo rm -f /etc/modprobe.d/usbhid.conf`

## How To Install/Remove with Deb Package

You can download and install with Gdebi following Deb package .

[aziokbd-dkms_1.0.0_amd64.deb](https://github.com/kelebek333/aziokbd-dkms/raw/master/aziokbd-dkms_1.0.0_amd64.deb)

You can remove with following command.

`sudo apt purge aziokbd-dkms`
