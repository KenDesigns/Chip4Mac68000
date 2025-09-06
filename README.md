# Chip4Mac68000 by KenDesigns

Pretty much what it says on the tin, a Chip8 Emulator for the original Motorola 68000 based Macintosh line! This is the first app written with a new bare metal SDK I am developing for the original 68000 based Macs, called Mac68000 SDK. This SDK is still under development and is not released yet.

## How do I run it?
### Real Hardware:

You MUST have one of the following models:

- Macintosh 128K
- Macintosh 512K
- Macintosh 512Ke
- Macintosh Plus
- Macintosh SE
- Macintosh SE FDHD
- Macintosh Classic

This WILL NOT run on any other Macintosh models. Do NOT try running this on a SE/30 or a Classic II or whatever, it will NOT work.

For a Macintosh 128K or 512K, the given 800K image will work with an external 800K FDD (no ROM upgrades are necessary thanks to custom bootloader magic).

You can load the program either using a FloppyEMU, or off a real floppy disk. If using the FloppyEMU, you must first format the SD card you are going to use with it, and then copy the disk image FIRST, before any other disk images. This is due to a bug in the FloppyEMU that causes bit-stream timing issues with fragmented files in a way that is incompatible with my custom bootloader. Copying the disk image first on a formatted disk guarantees no file fragmentation.

If you want to make a real floppy disk of this, you will need a FloppyEMU and a floppy disk. First, follow the directions above to copy the application disk image to the SD card. Then AFTER doing so, copy the "Copy II" application to the SD card. Use this Copy II application to then copy the image from the FloppyEMU to a real floppy disk (I recommend doing this with the "bit copy" setting although the sector copy with format should also work). Make sure to select the 800K disk copy option.

I have thoroughly tested this to work on a Macintosh 512K with a FloppyEMU and a Macintosh Plus with a real 800K floppy disk and everything works. I have done some testing on a Macintosh SE, although my SE has broken sound so I cannot confirm that it may work correctly (my ADB driver might accidentally mess with the sound driver but I have not been able to check yet). If this is the case, this will affect sound for all models with ADB, so that is the SE, SE FDHD and Classic. FWIW, I have confirmation from someone that sound works on their Classic (thank you TopherPerson from the TinkerDifferent Discord server)!

### Emulator:
Currently, as of September 2025, there are only 2 emulators accurate enough to run programs written bare metal with my SDK.

#### Snow
Make sure you are using the LATEST version of Snow. Snow has only very recently been updated to fix some bugs that made applications with my SDK unusable, so be sure to be on the latest version. After this, when setting up the emulated system, make sure to change "Mouse emulation" from "Absolute (memory patching)" to "Relative (hardware emulation)". You MUST make this change, or else the mouse will not work and worse, the emulated program will eventually crash.

By the way, if you are using literally any other Macintosh emulator (especially something like MiniVMac), I would HIGHLY, recommend ditching it for Snow. It is literally indescribably more accurate than those other emulators, which should only be used if your still on a Pentium II and Snow runs to slowly on that.

#### MAME
Honestly despite MAME being a little bit more accurate than Snow (as of September 2025), I would not recommend it due to the difficulty of setup. Assuming you have it setup, no tweaks are needed, except make sure not to use the emulated Mac Plus configuration specifically, as it has a bug where the keyboard doesn't work (I have no idea how they managed this when the rest of the earlier models have the same keyboard and work fine???).

## Acknowledgements
Thanks to the following people on the Tinker Different discord who have been graciously helping me test this and the SDK by running it on their machines:
- TopherPerson (Chris)
- 1Bit Fever Dreams
- Andy

Also thanks to the following people for help with the SDK:
- @smf- : Expert MAME developer and wrangler, helped me every time I needed to metaphorically squeeze MAME into a misshapen blob for testing
- @spicyjpeg : Writer of many a SDK himself, his SDK "ps1-bare-metal" was inspiration for parts of my SDK. He also has given lots of good advice to me on SDK development
- @nicolasnoble : My biggest opp, but also gives me good advice on all things programming so its ok ;)

Also extra big shout out to Grant, who caught the bug with the FloppyEMU in the first place. He asks that I give a shot-out to the RI Computer Museum, which you should totally visit if you happen to be nearby!
https://www.ricomputermuseum.org
