
# ALU Verilog Project

## Your name and netID
Name: Kesheng Wang  

NetID: kw457

## Description

This project implements a 32-bit Arithmetic Logic Unit (ALU) in Verilog. The ALU supports basic arithmetic operations including addition and subtraction, using two's complement representation. It also includes overflow detection.

## Modules

### 1. ALU
- **Inputs**:
  - `data_operandA` (32-bit)
  - `data_operandB` (32-bit)
  - `ctrl_ALUopcode` (5-bit)
  - `ctrl_shiftamt` (5-bit)
- **Outputs**:
  - `data_result` (32-bit)
  - `isNotEqual` (1-bit)
  - `isLessThan` (1-bit)
  - `overflow` (1-bit)
- **Functionality**: Performs addition or subtraction based on `ctrl_ALUopcode`.

### 2. Mux2to1
- **Inputs**:
  - `sel` (1-bit)
  - `a` (1-bit)
  - `b` (1-bit)
- **Output**:
  - `y` (1-bit)
- **Functionality**: 2:1 multiplexer to select between inputs `a` and `b`.

### 3. Full Adder
- **Inputs**:
  - `A` (1-bit)
  - `B` (1-bit)
  - `Cin` (1-bit)
- **Outputs**:
  - `Sum` (1-bit)
  - `Cout` (1-bit)
- **Functionality**: Computes the sum and carry-out of three 1-bit numbers.

### 4. RCA (Ripple Carry Adder)
- **Inputs**:
  - `in1` (16-bit)
  - `in2` (16-bit)
  - `cin` (1-bit)
- **Outputs**:
  - `sum` (16-bit)
  - `cout` (1-bit)
- **Functionality**: Performs 16-bit addition using a chain of full adders.

### 5. ALU Adder
- **Inputs**:
  - `data_operandA` (32-bit)
  - `data_operandB` (32-bit)
- **Outputs**:
  - `res` (32-bit)
  - `overflow` (1-bit)
- **Functionality**: Adds two 32-bit numbers and detects overflow.

### 6. ALU Subtractor
- **Inputs**:
  - `data_operandA` (32-bit)
  - `data_operandB` (32-bit)
- **Outputs**:
  - `res` (32-bit)
  - `overflow` (1-bit)
- **Functionality**: Subtracts two 32-bit numbers and detects overflow.
