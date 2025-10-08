A CPU without any instruction set.     
Opcode only has register address.     
Example 32 bit computer have 8 registers. So the Op code can select 8 32bit registers at the same time.     
It has only one Assembler code: R0,R1,R2,R3,R4,R5,R6,R7     
How it works.
     
Each register has a control register, which is not accable from the op code. this can be nop, add, move, div.. etc     
So the register control code is load from memory for each reister.  
IE:  Setup
     {
     LDcontroler R0, "ADD R0,R1,R3"     
     LDcontroler R1, "Jump on R0=zero to, @R1=$lable1"     
     LDcontroler R3, "Jump on R3=NotEq to 4, to @R4=$lable2"     
     }     
     R0,R1,R3 (executes ADD R0=R1,R3) and jump to #lable if R0 = Zero, Else Jump $lable2          
$lable1:  
    code....      
$lable2:          
    code....     
    
On cpu reset the Regiser control code is loaded from memory address 0x00000 ( or what ever user defines) 
 
Verilog      

