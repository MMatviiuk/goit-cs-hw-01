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

### Objective
Update an interpreter to support multiplication, division, and parentheses.

### Instructions
Update Lexer: Add support for MUL, DIV, LPAREN, RPAREN.
Modify Parser: Handle multiplication, division, and parentheses.
Update Interpreter: Process new operations.
__________________________________________________________________________________________________________________________________________________________________________________________________________________________________

To compile an assembly program using NASM (Netwide Assembler) and create a .COM executable, please follow these steps:

0. Install NASM & DOSBox
   
1.	Save the below assembly code in a file named calc2.asm.

2.	 Compile the file using NASM:
a)	navigate to the directory containing the file:
cd C:\1

b)	Compile the file:
nasm -f bin -o calc2.com calc2.asm

c)	Ensure that the calc2.com file is in C:\1 and does not have a .txt or any other unwanted extension.

4.	Open DOSBox.
a)	mount the directory:
mount c c:\1
b)	switch to the virtual disk:
c:
c)	run the program:
calc2.com

5.	Take a screenshot of the program's output.

```bash
org 0x100                ; Indicate that this is a .COM program

section .data
    a db 5               ; Define a = 5
    b db 3               ; Define b = 3
    c db 2               ; Define c = 2
    resultMsg db 'Result: $' ; Define string for result message

section .text
_start:
    mov al, [b]          ; Load b into AL
    sub al, [c]          ; Subtract c from AL
    add al, [a]          ; Add a to AL

    ; Convert result to ASCII (for single-digit numbers)
    add al, 30h          ; Convert number to ASCII character

    ; Print result message
    mov ah, 09h          ; DOS function to print string
    lea dx, resultMsg    ; Load address of resultMsg into DX
    int 21h              ; Call DOS interrupt

    ; Print result
    mov dl, al           ; Load result into DL for output
    mov ah, 02h          ; DOS function to print character
    int 21h              ; Call DOS interrupt

    ; Exit program
    mov ax, 4c00h        ; DOS function to exit program
    int 21h              ; Call DOS interrupt
```

Run Interpreter
python main.py
Verify
Test expressions with multiplication, division, and parentheses.
