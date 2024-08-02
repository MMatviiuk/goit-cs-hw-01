# goit-cs-hw-01
Домашнє завдання до модуля “Архітектура комп'ютерів”

# Computer Architecture Homework

This repository contains solutions for two tasks related to computer architecture.

## Task 1: Assembly Program

### Objective
Modify an assembly program to calculate `b - c + a`.

### Instructions
1. **Compile**:
   ```bash
   nasm -f bin -o calc2.com calc2.asm
   ```
Run in DOSBox:
bash
mount c c:\path\to\directory
cd c:
calc2.com
Verify the result and take a screenshot.

## Task 2: Interpreter Enhancement

## Objective
Update an interpreter to support multiplication, division, and parentheses.

## Instructions
Update Lexer: Add support for MUL, DIV, LPAREN, RPAREN.
Modify Parser: Handle multiplication, division, and parentheses.
Update Interpreter: Process new operations.
__________________________________________________________________________________________________________________________________________________________________________________________________________________________________
To compile an assembly program using NASM (Netwide Assembler) and create a .COM executable, follow these steps:

1. Install NASM
Ensure you have NASM installed. You can download it from the NASM official website or install it using a package manager if you’re on Linux.

2. Write Your Assembly Code
Save your assembly code to a file, e.g., calc2.asm.

3. Compile the Code
Use NASM to compile the assembly code into a binary .COM file. Open your command line interface (Terminal on Linux/macOS, Command Prompt or PowerShell on Windows) and navigate to the directory where your calc2.asm file is located.

Run the following command:

nasm -f bin -o calc2.com calc2.asm
Here's what each part of the command means:

nasm: The command to run the NASM assembler.
-f bin: Specifies the output format as a raw binary file (which is suitable for .COM files).
-o calc2.com: The output file name.
calc2.asm: The input file containing your assembly code.

4. Run the Program
Open DOSBox:

DOSBox is an emulator for running DOS applications. If you don’t have DOSBox installed, download and install it from the DOSBox website.
Mount the Directory:

In DOSBox, mount the directory where calc2.com is located as a virtual drive.
For example:
mount c c:\path\to\directory
Replace c:\path\to\directory with the actual path to your directory.
Change to the Mounted Drive:

Switch to the mounted drive:
c:
Run the Program:

Execute the program:
calc2.com

Run Interpreter
python main.py
Verify
Test expressions with multiplication, division, and parentheses.
