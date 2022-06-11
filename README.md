# rtl8852be_bt

## Introduction
This code is for realtek 8852BE bluetooth.  
I cloned original code from [Linux 5.15 Kernel LTS](https://www.kernel.org/) and change it a bit.   
It can now support Ubuntu 22.04 LTS(need more test).  
Any ideas are welcomed.  

## Prerequisites
```
build-essential 
linux-headers
bc
```

## Usage
### 1. Check your Bluetooth Device
```
$ lsusb
$ Bus 003 Device 005: ID 0bda:4853 Realtek Semiconductor Corp. Bluetooth Radio
```

### 2. Modify/Add your USB DEVICE in btusb.c
[Modify Here](https://github.com/HRex39/rtl8852be_bt/blob/5.15/btusb.c#L424)  
```
/* Realtek 8852BE Bluetooth devices */
{ USB_DEVICE(0x0bda, 0x4853), .driver_info = BTUSB_REALTEK |
               BTUSB_WIDEBAND_SPEECH },

// USB_DEVICE(0x____ , 0x____) is your ID name which shows in lsusb command
```

### 3. Save and Build
```
#Turn off your Security Boot in BIOS

make
sudo make install
reboot
```

## WHAT IS LINUX?
```
WHAT IS LINUX?

  Linux is a clone of the operating system Unix, written from scratch by
  Linus Torvalds with assistance from a loosely-knit team of hackers across
  the Net. It aims towards POSIX and Single UNIX Specification compliance.

  It has all the features you would expect in a modern fully-fledged Unix,
  including true multitasking, virtual memory, shared libraries, demand
  loading, shared copy-on-write executables, proper memory management,
  and multistack networking including IPv4 and IPv6.

  It is distributed under the GNU General Public License - see the
  accompanying COPYING file for more details. 
```
