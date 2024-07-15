mocoLUFA (MIDI firmware for Arduino)
======================
Fork of repository by morecat_lab (see information down below)


2024/07/15

based on LUFA-100807

This is a dual mode USB firmware for Arduino boards.
1) USB-MIDI (MocoLUFA)
2) Arduino-Serial

GETTING STARTED:

Build the firmware:

1. Download LUFA-100807 <br/>
	https://www.fourwalledcubicle.com/LUFA.php
2. Extract and add a .gitignore / adjust the .gitignore and add an exclusion for this project's root folder
3. Copy this whole folder into the folder LUFA_100807/Projects
4. Maybe you need to adjust the C / GCC include path list
5. In "Descriptors.c" set your desired vendor and device names (vendor and product strings)
6. Navigate in terminal into the project folder (not the LUFA root folder) and execute command "make all"
7. Check if the build process completed successfully or if certain errors are logged

-Tobias Zysk-

-------------------------------------

mocoLUFA (MIDI firmware for Arduino Uno)
----------------------
dualMocoLUFA Project
Copyright (C) 2013,2014,2015 by morecat_lab

2015/04/11
   
http://morecatlab.akiba.coocan.jp/lab/index.php/aruino/midi-firmware-for-arduino-uno-moco/?lang=en
  
based on LUFA-100807  

This is dual mode firmware for Arduino Uno.  
There are two mode on this firmware, USB-MIDI(MocoLUFA) and Arduino-Serial.  

INSTRUCTIONS  
1. Burn 16u2 on Arduino Uno.  
   check original document below.  
2. USB-MIDI firmware is started by default.  
3. To enable Arduino-Serial, place a jumper between PIN 4 (MOSI PB2) and PIN6 (grand) on ICSP connector for 16U2.  
   A reset is required to switch the firmware mode.  
  
-Yoshi  
  
-------------------------------------
original readme.txt from Arduino-Serial  
  
To setup the project and upload the Arduino usbserial application firmware to an ATMEGA16U2 using the Arduino USB DFU bootloader:  
	1. unpack the source into LUFA's Projects directory  
	2. set ARDUINO_MODEL_PID in the makefile as appropriate  
	3. do "make clean; make"  
	4. put the 16U2 into USB DFU mode:  
	4.a. assert and hold the 16U2's RESET line  
	4.b. assert and hold the 16U2's HWB line  
	4.c. release the 16U2's RESET line  
	4.d. release the 16U2's HWB line  
	5. confirm that the board enumerates as either "Arduino Uno DFU" or "Arduino Mega 2560 DFU"  
	6. do "make dfu" (OS X or Linux - dfu-programmer must be installed first) or "make flip" (Windows - Flip must be installed first)  

Check that the board enumerates as either "Arduino Uno" or "Arduino Mega 2560".  Test by uploading a new Arduino sketch from the Arduino IDE.
