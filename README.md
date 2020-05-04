Full guide for a macOS High Sierra Hackintosh on the Dell Inspiron 15 3558
---
# Getting Started
Download The master of this repo, this will include all files and folder for the completion of this tutorial

# Making the USB

This tutorial will use a mac to create the usb boot drive for this tutorial, if you do not have a mac google the way to make bootable usb drives for your specific OS.

### In the unzipped master folder of this repo find the file named 3558_usb.iso, keep this is a good location
### Insert you USB drive and open terminal and type
`diskutil list`
### Then find the usb drive that you just inserted it will be something like disk2

### We will be making two partitions on this usb, the first is the Clover efi which holds the bootloader
### The second is the partition that holds the macOS installer
### to do this run
`diskutil partitionDisk /dev/disk1 2 MBR FAT32 "EFI" 200Mi HFS+J "macOS Installer" R`
### Replace disk1 with whatever disk your usb was on, so if your usb was disk3 it would be /dev/disk3
### This make take some time depending, so be patient.
