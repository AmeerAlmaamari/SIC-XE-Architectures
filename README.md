# SIC/SICXE Assembler Project

## Overview

This project implements assemblers for the Simplified Instructional Computer (SIC) and its extended version, SIC/XE. The assemblers translate assembly language programs into machine code executable by the respective SIC and SIC/XE machines. This project includes functionality to handle instructions, directives, and generate object code.

## Project Structure

- `instfile.py`: Contains lists of instructions, formats, opcodes, and tokens used by both assemblers.
- `SIC Assember.py`: The main assembler for the SIC machine, handling the assembly process for standard SIC programs.
- `XE Assember.py`: The main assembler for the SIC/XE machine, including support for additional instructions and extended formats.

## Features

- **Instruction Set Support**: Both assemblers support a comprehensive set of instructions and directives as defined in `instfile.py`.
- **Symbol Table Management**: Efficient handling of symbols and labels within the assembly process.
- **Two-Pass Assembly**: Implements the two-pass assembly process to resolve forward references and generate object code.
- **Error Handling**: Basic error detection and reporting for undefined symbols, invalid instructions, and other common assembly errors.

## Getting Started

### Prerequisites

- Python 3.x
- Clone or download the project files

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-repository/sic-sicxe-assembler.git
```
2. Navigate to the project directory:
   ```bash
   cd sic-sicxe-assembler
```

### Usage
#### Assembling SIC/XE Programs
1. Prepare your SIC or SIC/XE assembly program and save it as `input.sic.`
2. Run the SIC or SIC/XE assembler:
```bash
python3 "SIC Assember.py"
python3 "XE Assember.py"
```
3. The assembler will generate an object code file and optionally a listing file with addresses and machine code.

## Files Description
### `instfile.py`
Contains the following lists:

- `inst`: List of instruction mnemonics.
- `instformat`: Corresponding instruction formats.
- `opcode`: Corresponding opcodes for the instructions.
- `token`: Token types for the instructions.

### `SIC Assember.py`
- Imports required modules and initializes variables.
- Defines `Entry` class for symbol table entries.
- Implements functions `lookup`, `insert`, and `init` for managing the symbol table.
- Reads input SIC file, processes each line, and performs two-pass assembly.
- Generates object code and handles output.

### `XE Assember.py`
- Similar structure to `SIC Assember.py` but includes additional support for SIC/XE specific instructions and formats.
- Defines `Entry` class with additional block attribute for handling program blocks.
- mplements functions `lookup`, `insert`, and `init` for managing the symbol table with extended features.
- Reads input SIC/XE file, processes each line, and performs two-pass assembly.
- Generates object code and handles output.



