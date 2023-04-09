# 4-Bit-Microprocessor 
4 bit microprocessor contains 3 major chunks including, 

# ALU
It is for performing addition , subtraction, AND, OR, and Xor operations on operands.
It`s mode can be selected by specific opcode using instruction decoder.

# Instruction Decoder
This part of microprocessor is to decode the instruction forwarded by ROM.
ROM forwards a specific 4 bit opcode to decoder. That opcode decides the address to be jumped on in decoder. Whatever present of that address in decoder is then moved to lines of decoder.

# ROM
PROM is a programmable ROM. Each instruction carries total 8 bits out of which MSB 4 bits are assigned to opcode and LSB 4 bits are for operand. We have used the splitter to slpit 8 bits into 2 halves.

# Selector
Then comes the selector circuit which selects that either we write operand from ROM in register or the output of ALU will be stored in register.

# Register File
It has 2 registers A and B, in which values are immediately loaded. The output of ALU operations is also loaded in any 4 bit register of it. It has a selection input connected to instruction decoder which decides which register is to be used.


# Display screen

It displays all the calculations we have made so far.

# Demo by example

For sake of demonstartion, 
We want to perform addition of 2, 4 bit numbers  3 and 4 by using our microprocessor by following these steps:

# ROM AND OPCODES

We made an 8 bit ROM, first 4 bits are assigned to opcode and other 4 bits are operand.

We assign opcodes for implementation of each command thrpough instruction decoder.

# OPERATIONS ON OPERAND

In first step the value 3 is to be loaded in Register B by LDI command. (LDI RB, 3), by enabling WE for B.

In next step we have to display 3 on screen, by enabling it through instruction decoder.

In next step we load the specific ASCII code for sign of "+" in both registers by load command and then display it to screen.

The load 3 again to register A and 4 to B, in two steps by enabling WE and S0/S1 of register file.

This time the write enable of Alu is activated.

When we assign the opcode of addition command and use it by instruction decoder then it adds the 2 numbers in ALU.

The sum of both numbers is then taken to Selector and then stored in register file, regA by enabling the selector mode, WE and turning S0 to 0.

In last step we again enable the dsiplay to show the output of sum on screen.

As result the sum of both numbers(7) will be displayed on the screen.
