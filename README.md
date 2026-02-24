# WARNING: 
To boot in **qemu on legacy bios** you need to put the **image first** and then the drive you're gonna be installing to and the drive you're installing it to must be **64GiB or larger** (20GiB or larger for linux), smaller drives may not work
# WARNING:
Once you boot into the OS, your partition may be smaller than your drive, you need to resize it for yourself, on windows you can use niubi partition manager, just diskmgr or other tool, on linux you can use gparted or some other tool. The job is up to you, i won't be answering issues regarding this, for some linux distros you will have to reinstall grub, here's how to do it

Alpine:
1. Boot from the img
2. Launch terminal
3. lsblk
4. look for your OS partitions (should be 300mb boot, 4gb swap and rest is OS)
5. mount /dev/(OS partition) /mnt
6. mount /dev/(boot partition) /mnt/boot (also mount it in /mnt/boot/efi if on uefi)
7. mount --bind /dev /mnt/dev
8. mount --bind /dev/pts /mnt/dev/pts
9. mount --bind /proc /mnt/proc
10. mount --bind /sys /mnt/sys (also mount --bind /sys/firmware/efi/efivars /mnt/sys/firmware/efi/efivars if using uefi)
11. chroot /mnt
12. grub-install --target=i386-pc /dev/(your drive) (or grub-install --target=x86_64-efi --efi-directory=/boot/efi --bootloader-id=GRUB if using uefi)
13. grub-mkconfig -o /boot/grub/grub.cfg

Arch:
1. Boot from the img or archiso (archiso recommended)
2. Launch terminal
3. lsblk
4. look for your OS partitions (should be 512mb boot, 8gb swap and rest is OS)
5. mount /dev/(OS partition) /mnt
6. mount /dev/(boot partition) /mnt/boot (also mount it in /mnt/boot/efi if on uefi)
7. arch-chroot /mnt (if using other iso, you have to do the steps like in debian or alpine)
8. grub-install --target=i386-pc /dev/(your drive) (or grub-install --target=x86_64-efi --efi-directory=/boot/efi --bootloader-id=GRUB if using uefi)
9. grub-mkconfig -o /boot/grub/grub.cfg|

Debian:
1. Boot from the img
2. Launch terminal
3. lsblk
4. look for your OS partitions (should be 300mb boot, 4gb swap and rest is OS)
5. mount /dev/(OS partition) /mnt
6. mount /dev/(boot partition) /mnt/boot (also mount it in /mnt/boot/efi if on uefi)
7. mount --bind /dev /mnt/dev
8. mount --bind /dev/pts /mnt/dev/pts
9. mount --bind /proc /mnt/proc
10. mount --bind /sys /mnt/sys (also mount --bind /sys/firmware/efi/efivars /mnt/sys/firmware/efi/efivars if using uefi)
11. chroot /mnt
12. grub-install --target=i386-pc /dev/(your drive) (or grub-install --target=x86_64-efi --efi-directory=/boot/efi --bootloader-id=GRUB if using uefi)
13. grub-mkconfig -o /boot/grub/grub.cfg

# How to install

1. Boot from the img
2. Press restore
3. Select the partition named Ventoy
4. Select `Windows-XX(10 or 11)-LTS-O-(UEFI/Legacy)` or (Distro)-LTS-O-(UEFI/Legacy) for linux
5. Select your drive 

# About OSes

**Windows 11/10 LTS O** is a custom build of Windows

# What does LTS O mean?

**LTS O** means **Long Term Support by Onogen**, this os is customized specifically to be

1. Light (Windows IoT Enterprise LTSC based)
2. Have long term support from microslop
3. Be fast
4. Have no bloat
5. No copilot or AI at all
6. Edge fully removed except webview

# What i will NOT be doing

1. Making LTS O build of an OS older than Windows 10
2. Making custom builds for some people specifically
3. Installing apps into the OS that some people don't need
4. Fixing bugs that Microslop made

You can post your suggestions on this github's issuesYou can post your suggestions on this github's [issues tab](https://github.com/TheRealOnogen/Project_LTS_O/issues).
I will not reply to suggestions i specified i won't be doing.

# Tools used:

1. Ventoy
2. Rescuezilla 
3. win11debloat

# What is Arch LTS O?

Arch LTS O is a custom Arch based distro, it has all the essentials and is meant to be arch for people whow want an easy install, it is not bloated, it includes

1. Nano
2. Ly (sddm on alpine)
3. KDE Plasma
4. Firefox and Konsole
5. NetworkManager
6. iwd and dhcpcd (not enabled, there for people who wanna use shell with wifi)
7. Grub Bootloader

# What i will NOT be doing

1. Making builds for specific people (except if LTS O builds of a specific architecture, depends tho)
2. Making LTS O builds of other distros
3. Fixing bugs in the kernel
4. Installing random packages
