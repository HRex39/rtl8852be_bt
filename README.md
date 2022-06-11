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

## Build
```
#Turn off your Security Boot in BIOS

git clone https://github.com/HRex39/rtl8852be_bt.git
cd rtl8852be_bt
make
sudo make install
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
