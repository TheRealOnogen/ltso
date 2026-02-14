# WARNING: 
To boot in **qemu on legacy bios** you need to put the **image first** and then the drive you're gonna be installing to and the drive you're installing it to must be **64GiB or larger** (20GiB or larger for linux), smaller drives may not work
# WARNING:
Once you boot into the OS, your partition may be smaller than your drive, you need to resize it for yourself, on windows you can use niubi partition manager, just diskmgr or other tool, on linux you can use gparted or some other tool. The job is up to you, i won't be answering issues regarding this

# How to install

1. Boot from the img
2. Press restore
3. Select the partition named Ventoy
4. Select `Windows-XX(10 or 11)-LTS-O-(UEFI/Legacy)`
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

1. Making builds for specific people
2. Making LTS O builds of other distros
3. Fixing bugs in the kernel
4. Installing random packages
