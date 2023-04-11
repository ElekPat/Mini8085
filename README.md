This is my Kicad version of http://www.malinov.com/Home/sergeys-projects/minimax8085, I called it V1.1.

![alt text](https://github.com/ElekPat/Mini8085/blob/main/MiniMax8085.jpg?raw=true)

MAX232 and DS1210 have been removed.
Added a 6 pin header for FTDI like external USB to serial adapter.

A prototype 2.54mm pitch zone was created (pads only on bottom face). You can see it populated here with a PIC16 acting as an I2C Master controller for the 8085 (requires changes to the original MiniMax8085 GAL).

For assembling source files, I use http://john.ccac.rwth-aachen.de:8000/as/ (Macro Assembler compatible with multiple target CPUs, see my other projects)

Use the following 2 command lines to generate a HEX file:
 - asw.exe -cpu 8085 -L source.asm
 - p2hex.exe source.p -k -F Intel
