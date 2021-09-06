# OPERATING SYSTEM ASSIGNMENT
Problem Statement : Download the latest stable Linux kernel from kernel.org, compile it, and dual boot it with your current Linux version. Your current version as well as the new version should be present in the grub-menu. 

# Following commands were executed to achieve the solution. 
1) uname -r (version of linux kernel) 
2) sudo apt-get update 
3) sudo apt-get install git fakeroot build-essential ncurses-dev xz-utils libssl-dev bc (install few packages) 
4) mkdir os_asg 
5) cd os_asg 
6) wget https://cdn.kernel.org/pub/linux/kernel/v5.x/linux-5.13.13.tar.xz (downloading source file) 
7) tar –xf linux-5.13.13.tar.xz (extracting .tar file) 
8) cd linux-5.13.13 
9) cp /boot/config-$(uname –r) .config  (config) 
10) make menuconfig (config) 
11) sudo apt install build-essential libncurses-dev flex bison libssl-dev libelf-dev (installation of dependencies) 
12) make -j5 (compilation and installation) 
13) sudo make modules_install (compilation and installation) 
14) sudo make install (compilation and installation) 
15) uname -r

