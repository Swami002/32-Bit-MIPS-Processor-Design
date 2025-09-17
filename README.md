# 32-bit MIPS Processor Design

This project implements a **single-cycle 32-bit MIPS processor** in Verilog. It supports **R-type, I-type, and J-type instructions** and includes modules for the **ALU, Register File, Instruction Memory, Data Memory, and Control Unit**.

## Features

- Supports basic instructions: `add`, `sub`, `addi`, `nop`, `lw`, `sw`, `beq`, `j`.
- **Single-cycle design** with PC, branching, and jump logic.
- ALU with arithmetic, logical, and comparison operations.
- Register file with 32 general-purpose registers.
- Instruction and data memory modules.
- Testbench with **clock/reset generation** and waveform dumping for simulation.
- Verified instruction execution using **EPwave**.

## Modules

- **MIPS32.v**: Top-level module connecting all components.
- **PC.v**: Program counter with synchronous reset.
- **InstrMem.v**: Instruction memory (can be initialized with instructions in Verilog or from a file using `$readmemh`/`$readmemb`).
- **RegFile.v**: 32-register file with read/write ports.
- **ALU.v**: Performs arithmetic, logic, and comparison operations.
- **DataMem.v**: Data memory with read/write control.
- **ControlUnit.v**: Generates control signals based on instruction opcode.
- **ALUControl.v**: Generates ALU control signals based on ALUOp and funct field.
- **tb_mips32.v**: Testbench for simulation with waveform dumping.

