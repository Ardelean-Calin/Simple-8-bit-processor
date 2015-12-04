This is a simple 8 bit processor design. It aims to be a useful tool from learning how microprocessors work from the ground up.

The processor is a [CISC](https://en.wikipedia.org/wiki/Complex_instruction_set_computing) processor with the following instructions implemented:

| Instruction   | Description                                   |
| -----------   | -----------                                   |
| `NOP`           | No operation                                  |
| `LOAD`          | Loads into A the value given by mem[MBR]      |
| `STORE`         | Stores A at mem[MBR]                          |
| `MOV B, A`      | Moves A into B                                |
| `MOV A, B`      | Moves B into A                                |
| `ADD A, B`      | Adds B to the accumulator                     |
| `SUB A, B`      | Subtracts B from the accumulator              |
| `AND A, B`      | Bitwise AND                                   |
| `OR A, B`       | Bitwise OR                                    |
| `XOR A, B`      | Bitwise XOR                                   |
| `INC A`         | Increments the accumulator                    |
| `CLA`           | Clears A using internal 0 register            | 
| `CLB`           | Cleard B using internal 0 register            |
| `SHL`           | Shifts A left by one                          |
| `SHR`           | Shifts A right by one                         |
| `PUSH A`        | Pushes A into stack                           |
| `POP A`         | Pops A from stack                             |
| `JUMP`          | Jumps to the instruction at mem[MBR]          |
| `IFEQ`          | Jumps if A == B                               |
| `IFZ`           | Jumps if A == 0 (register)                    |
| `IFL`           | Jumps if A < B                                |
| `INPUT`         | Loads into A the value in the INPUT register  |
| `OUTPUT`        | Loads into OUTPUT the value in the A register |
*Note: A is the accumulator.**

General Purpose Registers: A, B

Program Cycle:

* fetch instruction into MBR
* increment PC
* execute instruction 
