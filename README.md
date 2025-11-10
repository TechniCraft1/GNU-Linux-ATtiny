# GNU-Linux-ATtiny
This is an implimentation of an mini-rv32ima for the Arduino/ATtiny MCUs. This Project is not done yet, and wont work with the full kernel it is under development!

# What is there already:
-A semi working SD card code, that swaps into a new sector once for example JMP instructions are executed.
-A full implementation of chnlohrs mini-rv32ima
-A 512kb cache writing system with dirty flag
-A UART output of the emulator
-emulator halting instruction

# What needs to be done:
-better working SD read/write code
-writing to the sd card after a new sector is loaded
-several SD bug fixes

# What it can do yet:
-execute simple programs that dont write to a sector

# goals:
- Run the full linux kernel
- SPI output instead of Serial.print() for smaller ATtiny chips.
- Use smaller cache to make it run on >=1kb of RAM
- run at over 400hz on the ATtiny

WARNING: Make sure you use Logic Level converters or run the MCU at 3.3V
# SD card:
AVR:         SD:
13 PB5       SCK
12 PB4       MISO
11 PB3       MOSI
10 PB2       CS
