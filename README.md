# Chip4Mac68000

Pretty much what it says on the tin, a Chip8 Emulator for the original 68000 Macintoshes! This is the first app written with a new bare metal SDK I am developing for the original 68000 based Macs, called Mac68000 SDK.

It is compatible with the following models:

- Macintosh 128K
- Macintosh 512K
- Macintosh 512Ke
- Macintosh Plus
- Macintosh SE
- Macintosh SE FDHD
- Macintosh Classic

This WILL NOT run on any other Macintosh models. Do NOT try running this on a SE/30 or a Classic II or whatever, it will NOT work.

If you want to run this on an emulator, there is only one accurate enough to run this, MAME. This will NOT work on miniVMac.

If you want to make a real floppy disk of this, you will need a FloppyEMU and a 800K disk (this will only work loaded from an 800K disk, a 400K disk wont work). Use the Copy II application for Macintosh to then copy the image from the FloppyEMU to a real floppy disk (I recommend doing this with the "bit copy" setting although the sector copy with format should also work).

I have thoroughly tested this to work on a Macintosh 512K with a FloppyEMU and a Macintosh Plus with a real 800K floppy disk and everything works. I have done some testing on a Macintosh SE, although my SE has broken sound so I cannot confirm that it may work correctly (my ADB driver might accidentally mess with the sound driver but I have not been able to check yet). If this is the case, this will affect sound for all models with ADB, so that is the SE, SE FDHD and Classic. FWIW, I have confirmation from someone that sound works on their Classic (thank you TopherPerson from the TinkerDifferent discord)!

While I am thanking people, thanks to the following people on the Tinker Different discord who have been graciously helping me test this and the SDK by running it on their machines:
- TopherPerson (Chris)
- 1Bit Fever Dreams
- Andy

Also thanks to the following people for help with the SDK:
- @smf- : Expert MAME developer and wrangler, helped me every time I needed to metaphorically squeeze MAME into a misshapen blob for testing
- @spicyjpeg : Writer of many a SDK himself, his SDK "ps1-bare-metal" was inspiration for parts of my SDK. He also has given lots of good advice to me on SDK development
- @nicolasnoble : My biggest opp, but also gives me good advice on all things programming so its ok ;)

Anyways, thats all from me, please enjoy, and hopefully more programs are to follow!

-Ken Designs