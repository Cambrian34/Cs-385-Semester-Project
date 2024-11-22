# Digital Logic Design Modules

This repository contains Verilog implementations of fundamental digital logic design components. Each module is designed to perform specific operations, such as addition, multiplexing, or arithmetic logic unit (ALU) computations. These modules are useful for constructing and simulating complex digital systems.

---

## Table of Contents

1. [Half Adder](#half-adder)
2. [Full Adder](#full-adder)
3. [Multiplexers](#multiplexers)
    - 4x1 Multiplexer
    - 2x1 Multiplexer
    - 2-bit 2x1 Multiplexer
    - 16-bit 2x1 Multiplexer
    - 16-bit 4x1 Multiplexer
4. [Arithmetic Logic Unit (ALU)](#arithmetic-logic-unit-alu)
    - 16-bit ALU
    - 1-bit ALU
    - 1-bit ALU (Significant Bit)
5. [Register File](#register-file)
6. [16-bit Register](#16-bit-register)
7. [Decoder](#decoder)

---

## Half Adder

**Module Name:** `halfadder`

### Description
A combinational circuit that adds two 1-bit binary numbers. It outputs a sum (`S`) and carry (`C`).

### Ports
- **Inputs:** `x`, `y`
- **Outputs:** `S`, `C`

---

## Full Adder

**Module Name:** `fulladder`

### Description
Adds three 1-bit binary numbers (two inputs and a carry-in). It outputs a sum (`S`) and carry-out (`C`).

### Ports
- **Inputs:** `x`, `y`, `z`
- **Outputs:** `S`, `C`

---

## Multiplexers

### 4x1 Multiplexer

**Module Name:** `mux4x1`

### Description
A 4-to-1 multiplexer selects one of the four inputs based on a 2-bit select line.

### Ports
- **Inputs:** `i0`, `i1`, `i2`, `i3`, `select`
- **Output:** `y`

---

### 2x1 Multiplexer

**Module Name:** `mux2x1`

### Description
A 2-to-1 multiplexer selects one of two inputs based on a single-bit select line.

### Ports
- **Inputs:** `A`, `B`, `select`
- **Output:** `OUT`

---

### 2-bit 2x1 Multiplexer

**Module Name:** `mux2bit2x1`

### Description
A multiplexer that selects between two 2-bit inputs.

### Ports
- **Inputs:** `A`, `B`, `select`
- **Output:** `OUT`

---

### 16-bit 2x1 Multiplexer

**Module Name:** `mux16bit2x1`

### Description
A multiplexer that selects between two 16-bit inputs.

### Ports
- **Inputs:** `A`, `B`, `select`
- **Output:** `OUT`

---

### 16-bit 4x1 Multiplexer

**Module Name:** `mux4x1_16bit`

### Description
A multiplexer that selects one of four 16-bit inputs based on a 2-bit select line.

### Ports
- **Inputs:** `i0`, `i1`, `i2`, `i3`, `select`
- **Output:** `y`

---

## Arithmetic Logic Unit (ALU)

### 16-bit ALU

**Module Name:** `ALU`

### Description
A 16-bit ALU capable of performing various arithmetic and logical operations based on a 4-bit opcode.

### Ports
- **Inputs:** `a`, `b`, `op`
- **Outputs:** `result`, `zero`

---

### 1-bit ALU

**Module Name:** `ALU1`

### Description
Performs arithmetic and logical operations on single-bit inputs with configurable control signals.

### Ports
- **Inputs:** `a`, `b`, `ainvert`, `binvert`, `op`, `less`, `carryin`
- **Outputs:** `carryout`, `result`

---

### 1-bit ALU (Significant Bit)

**Module Name:** `ALUmsb`

### Description
Handles the most significant bit in multi-bit ALU operations, with support for carry and result propagation.

### Ports
- **Inputs:** `a`, `b`, `ainvert`, `binvert`, `op`, `less`, `carryin`
- **Outputs:** `carryout`, `result`, `sum`

---

## Register File

**Module Name:** `reg_file`

### Description
A register file with three 16-bit registers, supporting read and write operations.

### Ports
- **Inputs:** `rr1`, `rr2`, `wr`, `wd`, `regwrite`, `clock`
- **Outputs:** `rd1`, `rd2`

---

## 16-bit Register

**Module Name:** `register`

### Description
A 16-bit register that stores input data (`WriteData`) on the clock signal (`CLK`).

### Ports
- **Inputs:** `WriteData`, `CLK`
- **Outputs:** `ReadData`

---

## Decoder

**Module Name:** `decoder`

### Description
A 2-to-4 decoder used to enable specific outputs based on a 2-bit input.

---

## Usage

To use these modules:
1. Include the required module files in your Verilog project.
2. Instantiate the modules as needed in your top-level design or testbench.
3. Simulate using a Verilog simulator such as ModelSim or Vivado.

---

## License

This repository is open source and licensed under the MIT License.

---

