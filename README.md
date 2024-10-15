# Tektronix-4051-Emulator

![MONOPOLY](./MONOPOLY.png)

Based on the original ***Tektronix 405x Javascript Emulator*** by Dave Roberts and enhanced by Jon Stanley found here:
https://github.com/jonbstanley/Tek405xEmulator

plus many enhancements by Twilight-Logic in his fork here:
https://github.com/Twilight-Logic/Tek405xEmulator

---

# Table of Contents

- [Table of Contents](#table-of-contents)
- [Installation and Running the 4051 Emulator](#installation-and-running-the-4051-emulator)
- [Features](#features)
- [History](#history)

# Installation and Running the 4051 Emulator

- **Tektronix-4051-Emulator** requires a computer with at least 1024x800 graphics monitor and Chrome or other HTML5 web browser

- Download and unzip the 4051-Emulator zip file in this directory
- Download and unzip the FlashDrive zip file in this directory
- Run the 4051 Emulator by running the jsTEKTRONIX4051_universal.html file in the unzipped 4051 Emulator folder
- Your computer default web browser will launch the 4051 Emulator in a new tab
- Click the "!!mute button", then Click the "start" button at the bottom of the screen to start the 4051 emulator
- Click the "storage" button at the bottom of the emulator screen
  - select "4050 Flash Drive files" in the pulldown next to the Import button
- Click the "Import" button and click OK on the warning popup
  - use the computer file explorer pop-up window to navigate to the desired unzipped Flash Drive directory (ex: Games)
  - Click on the first file and press Shift and End keyboard keys to select all files in the directory and press Enter
  - Click "Close" on the Done popup window
  - Click "Cancel" on the storage window
- Click the "Auto Load" button on the 4051 Emulator
- This will load and run file 1 in this directory which is typically a menu program

# Features

I renamed this project Tektronix 4051 Emulator, since it is limited to emulating the Tektronix 4051 hardware:
- Motorola 6800 CPU with 800KHz clock
- 32KB of RAM
- 32KB of Tektronix 4050 BASIC ROM
- 1024x780 vector graphics resolution

Twilight-Logic added several features to the original 405x Emulator including:

- **All 4051 Option ROMs!**
  - 4051R01 Matrix Functions
  - 4051R05 Binary Program Loader
  - 4051R06 Editor
  - 4051R07 Signal Processing I
  - 4051R08 Signal Processing II
  - 4051R12 Graphics Enhancement
  - 4051R14 GPIB Enhancement
  - 4051 DDT51.8 6800 Assembly language Debugger
  - 4051 Extended BASIC
  - 4051 Extended Fonts
- **Flash Drive - Mass Storage**
  - Emulates an external Tektronix 4924 GPIB Tape Drive 
    - Multiple Flash Drives allow one file open on each drive for multiple reads or writes
    - Huge files (>500KB)
- **Scalable Vector Graphics**
  - Scales to the web browser window size (top button on top left corner of emulator window)
  - Three vector & text pixel modes (third button on top left corner of emulator window)
    - Quad Pixel 'dots' in vectors and text (Default and best for most 4050 programs)
    - Quad Pixel 'dots' in text and single pixel dots in vectors (best for viewing bitmap pictures)
    - Single Pixel 'dots' in vectors and text (matches original 405x Emulator text and vector size)
- **Emulator OverClock**
  - 1x, 2x, 5x, 10x, 20x, 50x, 100x (middle button on top left corner of emulator window)
    - 1x provides 4051 performance
    - 10x provides 4052 or 4054 performance
    - Above 10x may not scale further - limited by computer CPU performance (example - Raspberry Pi with Chromium browser)

---

# History

This emulator was initially created by Dave Roberts in 2017 and posted on github by Jonathan Stanley in 2018.

My first personal computer experience was using a Tektronix 4051 at work in the late 1970's.  I really enjoyed learning Tektronix 4050 BASIC and contributed a cubic spline interpolation program to the Tektronix application library.

I acquired a Tektronix 4052 and 4054 computer around 2000 and began creating a tape with 4050 games from listings I had printed at work.  I found a couple of people through the early internet that had 4051 computers and we exchanged the games tapes, but then my interest wained until I found Dave and Jonathan working on a 4051 Emulator on the vcfed dot org "Other" forum.

The achilles heel of the 4050 computers is the quarter-inch (QIC) data tape cartridge internal drive belt.  These drive belts are now over 40 years old (the 4051 was introduced in 1975 with these cartridges) and most of the cartridges have broken drive belts.  This belt was created by 3M from the same material as the tape and cut out as a ring and formed into a belt.  Since the drive belt contacts the oxide side of the tape - when the belt disentegrates it tends to also pull the oxide off the tape where it was in contact with both tape reels - causing data loss.

I decided in January 2018 to try to design a replacement for the 4050 tape using a microSD card for storage and an Arduino as the GPIB tape device.  I found an AR488 GPIB Arduino project on eevblog and contacted the software developer (Twilight Logic) about helping me design a GPIB Flash Drive emulating the Tektronix 4924 GPIB tape drive - which was fully supported in Tektronix 4050 BASIC.

We got the Flash Drive working with all three models of the Tektronix 4050 - the original 4051 and second generation 4052 and 4054 computers.

I then asked him if he could add the Flash Drive software to the 405x Emulator - and he also added the other featured mentioned above at my request as I began using his experimental version of the 405x Emulator to develop many of my latest 4050 programs including finishing the MONOPOLY game I had started in 1979 on the 4051!

I believe this version of the emulator truly provides 100% compatibility with the 4051.

I hope you enjoy it as much as I do.
