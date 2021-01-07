# CWDSDK
CWDSDK (Chris' Web Development Software Development Kit) is a program that uses a VM (CSDKVM) and a compiler (CSDKC) to create a web development system that can be closed source without needing to set up a web server using Node.JS or similar applications. 

(Used to be called CSDK (Chris' Sorce Development Kit) until I found out that the name was trademarked by Oracle Corporation (Client SDK), I do NOT wanna mess with them, especially with trademarks, so I changed it to CWDSDK. )

This project uses an open source software called p5.js (https://p5js.org/), which is in no way mine and is used in this project. 

Instructions (actual code used): 
//USAGE; DESCRIPTION - implemented yet?

//(please use raw mode on github)

var I_NOP = 0x0; - yes
var I_MOVRN = 0x1; //MOV register value; R_register'S VALUE BECOMES value - yes
var I_MOVRR = 0x2; //MOV register register2; R_register'S VALUE BECOMES R_register2'S VALUE - yes
var I_MOVRL = 0x3; //MOV register location; R_register'S VALUE BECOMES memory[location]'S VALUE - yes
var I_MOVLR = 0x4; //MOV location register; memory[location]'S VALUE BECOMES R_register'S VALUE - yes
var I_MOVLN = 0x5; //MOV location number; memory[location]'S VALUE BECOMES number - yes
var I_ADDRN = 0x6; //ADDRN register number; register += number - yes
var I_ADDRR = 0x7; //ADDRR register register2; register += register2'S VALUE - yes
var I_SUBTRN = 0x8; //SUBTRN register number; register -= number - yes
var I_SUBTRR = 0x9; //SUBTRR register register2; register -= register2'S VALUE - yes
var I_SETDRAWATTR = 0xA; //SETDRAWATTR attribute value; attribute'S VALUE BECOMES value - yes
var I_MSDRAWATTR = 0xB; //MSDRAWATTR x0val y0val x1val y1val rval gval bval; SETS ALL DRAW ATTRIBUTES BY NUMBER (Mass Set Draw Attributes) - yes
var I_MSDRAWATTRR = 0xC; //MSDRAWATTRR x0val y0val x1val y1val rval gval bval; SETS ALL DRAW ATTRIBUTES BY REGISTER - no, may be removed
var I_JMP = 0xD; //JMP memorylocation; PC = memorylocation - yes
var I_JSR = 0xE; //JSR memorylocation; PCRET = PC, PC = memorylocation - no
var I_RTS = 0xF; //RTS; PC = PCRET - no
var I_REFRESH = 0x10; //REFRESH; FUNCTIONALLY THE SAME AS NOP BUT OPTIMIZED FOR REFRESHING FRAMES - no
var I_CMP = 0x11; //CMP register number; COMPARE register TO number AND SET ALL FLAGS ON REGISTER FL - no
var I_BEQ = 0x12; //BEQ memorylocation; IF CMP PASSED EQ, PC = memorylocation - no
var I_BNE = 0x13; //BNE memorylocation; IF CMP PASSED NE, PC = memorylocation - no
var I_BLT = 0x14; //BLT memorylocation; IF CMP PASSED LT, PC = memorylocation - no
var I_BLE = 0x15; //BLE memorylocation; IF CMP PASSED LE, PC = memorylocation - no
var I_BGT = 0x16; //BGT memorylocation; IF CMP PASSED GT, PC = memorylocation - no
var I_BGE = 0x17; //BGE memorylocation; IF CMP PASSED GE, PC = memorylocation - no
var I_CLS = 0x18; //CLS; CLEAR SCREEN - yes
var I_DRAW = 0x19; //DRAW mode; (mode 0): draws and refreshes, (mode 1): draws without refreshing. Draws based on drawattr insts - yes
var I_SETDRAWATTRR = 0x1A; //SETDRAWATTR attribute R_register; will add desc later - yes
var I_HALT = 0xFFFF; //HALT exitcode; running = exitcode, execution full stops - yes


1/5/2021 - Working on CWDSDKVM, CSDKC has not been planned out yet and might be discontinued at a later date, but hopefully not. 

1/6/2021 - Moved different parts of program to multiple files for orginization. 

Also 1/6/2021 - Changed the name so I don't get sued. 
