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
- [Game board](#game-board)
- [Features Not Supported](#features-not-supported)
- [History](#history)

# Installation and Running the 4051 Emulator

- **Tektronix-4051-Emulator** requires a computer with at least 1024x800 graphics monitor and Chrome or other HTML5 web browser

- Download and unzip the 4051-Emulator zip file in this directory
- Download and unzip the FlashDrive zip file in this directory
- Run the 4051 Emulator by selecting the jsTEKTRONIX4051_universal.html file in the unzipped 4051 Emulator folder
- Your computer web browser will launch the 4051 Emulator in a new tab
- Click the "!!mute button", then Click the "start" button at the bottom of the screen to start the 4051 emulator
- Click the storage button at the bottom of the emulator screen
  - select "4050 Flash Drive files" in the pulldown next to the Import button
- Click the Import button and click OK on the warning popup
  - use the file explorer pop-up window to navigate to the desired unzipped Flash Drive directory (ex: Games)
  - Click on the first file and press Shift and End keyboard keys to select all files in the directory and press Enter
  - Click Close on the Done popup window
  - Click Cancel on the storage window
- Click the Auto Load button on the 4051 Emulator
- This will load the file 1 in this directory which is typically a menu program

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



  - If you don't have a Tektronix 4050 computer - you may enjoy playing my Monopoly game on the **latest Tektronix 405x Emulator** [Latest 405x experimental web-browser based emulator](https://github.com/Twilight-Logic/Tek405xEmulator/blob/master/experimental/JonStanley-Mod-Storage-Pix-20240427.zip).  Supported web browsers include Chrome, Firefox and Edge.  Follow my instructions in this post https://forum.vcfed.org/index.php?threads/tek-405x-web-browser-emulator.62548/post-1357155 - be sure to **Click to Expand** the instructions in my previous post but use my link above to download the latest version of the 405x emulator.  The 405X Emulator includes 32KB of RAM, 32KB Tek 4050 BASIC ROM, the R12 option ROM Pack, and GPIB Flash Drive but only supports importing a single directory of 4050 Flash Drive files.  I used this specific emulator to develop my Monopoly game.  To speed up development, I typically increase the emulator speed from the default 1x 4051 to at least 10x which is close to the performance running Monopoly on my 4054A computer.  Use the PC or MAC function keys 1-4 and 8 to operate the game running on the emulator.

- My Monopoly game uses the Tektronix User Definable Keys 1-4 and 8.

- To enable the game on a 4050 computer with my GPIB Flash Drive to use a Vectrex gamepad in addition to the UDK keys, after the game is loaded, press the BREAK key to stop the program and type 6110 and press the RECALL LINE editing key and then press the RUB OUT key to delete the TURN characters and type M to change the text to REM and press the RETURN key to save the change.  Now you can use the Vectrex gamepad buttons 1-4 to perform the same operations as pressing UDK 1-4.

----------------------------------

# Game Board
(yellow numbers on screenshot below correspond to numbered list below) 

![MONOPOLY](./Wilma%20is%20bankrupt%20-%20GAME%20OVER-markups.png)

* **Player**
 1. Player **TOKEN** is first initial of player name (up to 6 characters)
 2. Blinking Player **TOKEN** is current player

* **Action Keys** (UDK on Tek keyboard, Function keys on PC or MAC with 405x Emulator)
3. **F1** **ROLL** dice or **CONTINUE** (by clearing screen for next player or continues to next action)
4. **F2** **BUY** property at the current player location or buys a house or hotel on an owned property group
5. **F3** **VIEW Assets** displays list of asset prices - used for Income Tax in addition to player cash
6. **F4** **USE Jail Card** if player is in Jail and has a Get Out of Jail card
7. **F8** **QUIT** will stop the game and reload the Flash Drive MAIN MENU

* **Property**
8. Property Owner marked with **Owner TOKEN**
9. Properties in the same property group have the same **dashed UNDERLINE** under each property name
10. When all properties in a property group are owned by the same player the group has a **group outline** around the **Owner TOKENs**

* **Game Messages**
11. Show which property the current player is on.  At the start of each turn - the "Deed" area is blank and the player can use any of the five Action Keys.
12. After F1 is pressed, the two dice are displayed with a total of the two dice and the player **TOKEN** is advanced that number of spaces and then the name of the property is displayed along with the property DEED in the middle of the screen.
13. If that property is owned, the player pays the rent as shown on the deed.

* **Houses and Hotel**
14. After all the properties in a property group has the same owner, the owner may buy a house for any of the properties in that group. You must buy houses evenly following the standard Monopoly rules.  After four houses are on all the properties in a group you may buy a hotel one or more of the group of properties.

* **JAIL**
15. There are four jail cells - one for each possible player starting from the right cell for player1.
16. Possession of a Get Out of Jail card is a number displayed at the top of the jail cell column for that player.
  
----------------------------------

# Features Not Supported
Limited 32KB memory space for more features to be compatible with the 4051 is the primary reason.

 1. MORTGAGE and UNMORTGAGE are not supported.    
 2. SELL and AUCTION are not supported.

----------------------------------

# History
I started writing a Monopoly game on a Tektronix 4051 in 1979 - but ran out of 32KB of 4051 memory just displaying the Monopoly board graphics in Tektronix 4050 BASIC.  I made a hard copy printout of my program using a Tektronix 4631 Hard Copy unit attached to the 4051. 

![MONOPOLY orig scan](./Original%20Monopoly%20page1%20scan.jpg)

The 4051 and 4052 had a 12" flat screen storage tube CRT with addressable vector resolution of 1024 by 780. The 4054 and 4054A had a 19" curved screen storage tube and different display hardware that accelerated all graphics 10x over the 4052/4052A.

This screenshot shows my original Monopoly game board layout.  The 4051 and 4052 use dot matrix for text, so my program put the text for the properties at the top and bottom of the screen as shown.

![MONOPOLY](./my%20original%20Monopoly%20game%20board.jpg)

My completed game board is completely redesigned and used a Tek 4050 BASIC program that creates Leroy character set vector lettering at any size and any rotation angle!

Since I needed to reduce the size of the BASIC program statements, I use the 4050R12 Graphics Enhancement ROM Pack and BASIC programs I created to use BASIC MOVE and DRAW commands for the vectors and then an R12 CALL "AGIN" X,Y command to capture the X,Y coordinates in GDUs (native 130,100 graphic display units). Next each X,Y vector is saved in 3 byte R12 format with the R12 CALL "CHANGE",D,D$ where D is dimensioned as D(2) with D(1)=-X and D(2)=-Y.  The resulting vector string combining multiple MOVE and DRAW vectors was then written to a single binary data file.

All the Monopoly board lines, text, and images like the Jailer and Free Parking are in a single file 42 with a size of 17613 bytes representing about 5800 move or draw X/Y vectors - since the Tek 4050 BASIC binary data format adds a two byte header and one byte trailer to each data block.  The two byte header includes the length of the binary string.  The BASIC programs I created to make each of the binary files for the deeds include an end of card string |EOC| which my code uses to know the number of lines of text displayed on the card have all been read and the deed display code is done.

My Monopoly BASIC program is the largest Tektronix BASIC program I have written and I learned a lot of 4050 BASIC tricks to move as much graphics data and numeric data to external files to allow the most space for the Monopoly game logic.

Here is a photo of my 4054A running my MONOPOLY game:

![4054A MONOPOLY](./4054A%20MONOPOLY.JPEG)

I hope you enjoy this game as much as I do!


Loading the emulator with a BASIC program is accomplished through the browser interface
and the use of an emulated GPIB device (#1). There is also a Real Time Clock
configured as GPIB device #2.

Some of the keyboard keys are a bit 'wonky' at this point in time (!) as is
some of the screen display (for example the blinking cursor). Consider this
release as a pre-Alpha... The emulator is also considerably faster than the
original Tektronix 4051 machine. This is generally good news - except when
trying to pilot the Lunar Lander down (where this is virtually impossible)!

This emulator was written on an Apple iMac with the Safari browser. The emulator
requires a browser that is HTML 5 compliant (as some of the features used for
loading the BASIC program into the emulator). I have saved the source files in
such a manner that they should be readable and modifiable on a Windows platform - 
although I have not actually tested this out.

To run the emulator - double-click on the 'jsTEKTRONIX4051.html' icon. Your browser
should start and you should be presented with a large (1024 by 1024) black screen.
Scroll down a bit and you should find a button marked [start]. Click the [start] 
button. A little bit of diagnostic text (DER: MC6800.js >>>>> CRTRST: <<<<<) should 
appear in the debug log window below the button.

You should also see a blue square in the top left-hand corner of the screen. This is
(or will be when I have finished it!) the flashing green cursor...

Congratulations, the emulator seems to be running...

To load a BASIC program from the host operating system, the following procedure should
be followed:

Scroll down a bit to the buttons again.

Click the [Choose File] button and navigate to the directory containing the LINES.txt
file. Select this file. A message should appear in the debug log window as follows
"Selected file loaded from host operating system.".

In the Tektronix window type the command 'OLD @1:' followed by the <RETURN> key. The
selected BASIC program should be loaded into the emulator and the blue cursor should 
reappear on the next line. Type RUN and you should be away...

If you have tried the above procedure without reading to here - you will have identified
a problem with the keyboard. I have tried my best to map the Tektronix 4051 key matrix
to a 'standard' PC keyboard - but failed dismally in a number of areas! This is also not
helped by the shifted characters on a 'standard' keyboard being different to those on the
Tektronix keyboard either! I have mapped the keys as follows (again, noting that these
are off my iMac keyboard and not a PC). Also, I have a wired keyboard on my iMac and not
the wireless one - so I have access to the numeric pad.

Tektronix @         = Keyboard `
Tektronix :         = Keyboard '
Tektronix PAGE      = Function key 13.
Tektronix RUBOUT    = <DELETE> key.
Tektronix BREAK     = Function key 14.
Tektronix CLEAR     = Function key 15.
Tektronix AUTO NUM  = Function key 16.
Tektronix STEP PROG = Function Key 17.

If you hate me for this mapping (!) you have the source code so you can change it
yourself. Look for the function this.HandleKeyboardEvent in the file TEKTRONIX4051.js.

The CAPS LOCK, Control and Shift keys work - albeit with some limitations on the
characters that are actually displayed! I would suggest typing the characters on your 
keyboard and seeing what appears on the emulated Tektronix screen as a start.

You can't edit programs on the Tektronix emulation and save them back to the PC's disk.
Standard HTML and Javascript prohibits this. My expectation is that people will have
(or edit) the Tektronix BASIC programs using their favourite text editor on the PC and
download the program to run on the emulator.

I hope you find this emulator of interest. If you do, have identified bugs or have
helpful suggestions for improvement then please contact me at: 
daver21145 AT gmail DOT com - with text / character conversions as appropriate.

Regards,

Dave
