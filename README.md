I CPU without any instruction set.
Opcode only has register address.
Example 32 bit computer have 8 registers. So the Op code can select 8 32bit registers at the same time.
It has only Assembler one assembler code: R0,R1,R2,R3,R4,R5,R6,R7
How it works.
the option is loaded in to the register side controler. this can be nop, add, move.. etc
So the code is load from memory in the side  controle register.  
IE:  Setup
     {
     LD R0, ADD R0,R1,R3
     LD R1, Jump on R0=zero @R1
     LD R3, Jump on R3=Notequ 4 @R3
     }
     R0,R1,R3 (executes ADD R0=R1,R3) and jump to #lable if R0 = Zero, Else Jump $lable2
     
Verilog 

