# Cs-385-Semmester-Project


#16 Bit Mips Processor
#5 Stage pipeline



#Description:

This Verilog code implements a 16-bit pipelined MIPS processor. A pipelined processor divides the instruction execution cycle into stages, allowing multiple instructions to be processed simultaneously. This implementation uses a five-stage pipeline:

-Instruction Fetch (IF): Fetches the next instruction from memory.
-Instruction Decode (ID): Decodes the instruction and reads operands from the register file.
-Execute (EX): Executes the arithmetic or logical operation.
-Memory Access (MEM): Accesses memory for load or store operations.
-Write Back (WB): Writes the result to the register file.
##Modules and Components:

#The processor is composed of several interconnected modules, including:

-Instruction Memory: Stores the instructions to be executed.
-Data Memory: Stores data.
-Register File: Stores data in registers.
-Arithmetic Logic Unit (ALU): Performs arithmetic and logical operations.
-Control Unit: Generates control signals based on the instruction.
