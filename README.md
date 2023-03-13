
***

# BerryBoot

BerryBoot is an advanced GUI bootloader for the Raspberry Pi that is designed for heavily partitioned devices (up to 512 partitions) with a cool 3D dimensional interactive berry, whose seeds each represent a partition.

***

## Design goals

- [ ] Keep the entire distributed bootloader under 1,000,001 bytes (1.00 megabyte)
- [ ] Enable 3D graphics at the boot level
- [ ] Make the design resemble a raspberry

***

## GUI

A 3D raspberry, with a different operating system partition on each seed

### Background

**Default:** Green gradient

### Controls

**Controls:** `Up arrow key`, `Down arrow key`, `Left arrow key`, `Right arrow key`, `ENTER key`, `F8 key`

The berry is to move like a globe.

### The leaf

Just a texture piece, make sure it isn't covering the seeds

### The seeds

Once a seed is hovered over, information on the detected partition will display to either the right, left, top, or bottom of the screen (depending on the preference in the configuration file)

### Extras

[See cosmetics/tweaks](/Cosmetics/)

***

## Configuration tool

Work in progress (a desktop application for the Raspberry Pi that initializes the bootloader)

***

## Possible problems with the concept

- It may be too advanced of a GUI at the pre-boot level
- Support for many partitions required for adequate interface
- - Solution: Græy out all seeds that don't contain data

Render all partitions upon writing with the configuration tool, non-existant partitions are to be græyed out (not a working solution, as duplicates will show up, and overflow the seed limit of the berry)

**Multiple berries?**

A configuration for a second Raspberry Pi under the same device (not feasible)

***

## Languages

BerryBoot is written in:

- Assembly, C (bootloader)
- Python, Berry (configuration tool)

***

## FAQ

### Q: Why not just make a GRUB modification?

**A:** Some features aren't possible with GRUB, such as 3D animation. BerryBoot is its own GRUB, although it will be a heavy bootloader. 

### Q: Why the longer startup time?

**A:** This is a very advanced bootloader, and the design goal makes the longer startup time worth it for the GUI improvement. If not, you don't need this bootloader. Just use the default one that comes with your Raspberry Pi installation if you don't want to wait longer for each startup.

***

**File version:** `1 (2023, Sunday, March 12th at 6:40 pm PST)`

***
