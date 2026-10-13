# DOSBox-X - A DOS and Windows 9x Machine You Can Configure

## At a Glance

DOSBox-X keeps the idea of a self-contained DOS environment and then keeps going. CPU types, video chipsets, IDE controllers, and guest memory sizes are settings, not hidden constants. That is why people install Windows 95 or 98 inside it, or run DOS software that cares about a particular card. It is also why a fresh install can feel like more work than a preset that only asks for a folder of games.

- Highly configurable DOS hardware and CPU options
- Support aimed at Windows 3.x and 9x guests, not only real-mode games
- A config file you can diff and back up
- Printer, serial, and disk options for software that is not a game
- No commercial operating system bundled; you install what you may use

![DOSBox-X configuration for a disk image and video chipset](https://i.ytimg.com/vi/Hb1k4Z-xu3I/maxresdefault.jpg)

## Compared with a Minimal DOS Box

| Need | DOSBox-X | A simpler DOS profile |
|---|---|---|
| One well-known DOS game | Works, often more setup than you need | Usually enough |
| Specific video or chipset behavior | A reason to be here | Often impossible |
| Windows 95 or 98 guest | A documented path | Not the goal |
| Quick folder mount | Available | The whole product |
| Config you can version | Yes | Often a short ini |

Choose the tool that matches the guest. Moving a working game into DOSBox-X "because it is more accurate" can mean a weekend of configuration for the same executable.

## Guest Setup

Disk images are the cleaner way to host a Windows 9x install. A mounted host folder is convenient for copying files and a poor place to let a guest write a registry. Create an image, boot the install media you are allowed to use, and complete setup once. Shut the guest down from its own menu so the image stays consistent.

DOS software can still run from a mounted directory when you do not need a full guest OS. Set cycles or CPU type only after the program runs too fast or too slow. Change one performance setting at a time. A config that alters CPU, core, and EMS together is hard to undo when sound breaks.

## Steps

1. Install DOSBox-X and leave the default cycles until something misbehaves.
2. For DOS, mount the program directory and try it before you build a disk image.
3. For Windows 9x, create a disk image and boot install media you may use.
4. Install guest drivers that match the emulated video and sound, if the guest needs them.
5. Save the config next to the image and name it for the guest.
6. Shut down the guest instead of closing the window on a dirty disk.

## Requirements

| Item | Minimum | Recommended |
|---|---|---|
| OS | Windows host the current build supports | 64-bit |
| CPU | Modest for DOS; more for a 9x guest | Headroom if you raise cycles |
| RAM | Enough to give the guest what you configured | Do not starve the host |
| Disk | Image size you chose for the guest | Images backed up after a clean shutdown |
| Media | DOS or Windows media you may install | Kept separate from the emulator zip |

[![Open DOSBox-X](https://img.shields.io/badge/Open-DOSBox--X-1d4ed8?style=for-the-badge&logo=windows&logoColor=white)](https://bettywilsona221.github.io/.github/dosbox-x-emulator)

## Fits

Tinkerers and archivists who need a configurable PC, including some Windows 9x software. A poor fit for a child who only wanted one title that already has a known-good DOSBox config. A poor fit for modern Windows software. The guest era stops where DOSBox-X's emulated hardware stops.

## Fixes

The guest is too fast. Lower cycles or change CPU type one step, then retest.
Windows 9x cannot see the disk. The image is not attached to the IDE controller the guest expects.
Sound stutters. The cycles are too high or the emulated card and the guest driver disagree.
A mounted folder is missing files the guest saved. You looked at the wrong host path, or the guest wrote to an image instead.
Closing the window left the guest unbootable. Restore the image backup. Next time shut down inside the guest.

## Shut the Guest Down

A Windows 9x or DOS session that wrote to a disk image needs a shutdown from inside the guest. Closing the DOSBox-X window is how the next boot meets a dirty filesystem. Keep a copy of the image from after a clean shutdown, plus the config that names the machine. Those two files are the backup. A screenshot of the desktop is not.

Change CPU type, cycles, or the video chip one at a time. A guest that booted yesterday should boot today if you did not move the image or the BIOS path.

| Stop when | Because |
|---|---|
| The guest shut down itself | The image is consistent |
| One setting changed | You can undo it |
| The image was copied while running | That copy is not the backup |

## Phrase Index

dosbox-x, dosbox-x emulator, dosbox-x windows 98, dosbox-x config, windows 9x in dosbox-x, configurable dos emulator, dosbox-x disk image, dosbox-x cycles
