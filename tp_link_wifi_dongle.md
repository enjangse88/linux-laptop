Laptop type: X220
OS Type: Debian 11 - Bullseye
USB Wifi: TPlink 

issue: can not load firmware 
firmware: failed to load rtlwifi/rtl8188eufw.bin
[ 3001.819838] r8188eu 1-1.4:1.0: Direct firmware load for rtlwifi/rtl8188eufw.bin failed with error -2 

work-around:
su root
mkdir /lib/firmware/rtwifi
sudo wget https://github.com/lwfinger/rtl8188eu/raw/c83976d1dfb4793893158461430261562b3a5bf0/rtl8188eufw.bin  -O /lib/firmware/rtlwifi/rtl8188eufw.bin
reboot

check dmesg 
lsusb
iwwifi

reboot
