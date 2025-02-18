# chandanpoojary-sahyadri-ece
Repository for Samsung RISC-V Talent Development Program

The program harnesses the RISC-V architecture and employs open-source tools to instruct individuals on the design of VLSI chips and the fundamentals of RISC-V

BASIC DETAILS:

Name: Dheeraj

College: Sahyadri college of Engineering and management,Adyar,Mangalore-575007

College mail: chandan.ec23@sahyadri.edu.in

Email ID: chandanpoojary1@gmail.com

GitHub profile:https:https://github.com/chandanpoojary11

Linkedin profile:https://www.linkedin.com/in/chandan-m-67515b293?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=ios_app

Task1

![image](https://github.com/user-attachments/assets/032e7b65-5985-48e3-8284-10f8f5fbf73f)

![image](https://github.com/user-attachments/assets/f3fc7435-efeb-41ca-9b6b-9237a37c9382)

![image](https://github.com/user-attachments/assets/9c60b4b1-5fee-4d39-9e3e-84a3fe358324)

Task2

![image](https://github.com/user-attachments/assets/15ac80a3-d6b0-48dd-a635-bcf44f5608aa)

![image](https://github.com/user-attachments/assets/08b5306e-c600-4188-a7b2-aa37c57441ea)

Task3

Task 3.1 

![image](https://github.com/user-attachments/assets/cc391856-1330-4eba-9fb4-f064e79374e2)

Task 3.2

![image](https://github.com/user-attachments/assets/f2938b1a-5f36-43f3-96b4-5949641f7c1b)


RISC-V Instruction Types and Fields
RISC-V instructions are categorized into different types based on how their fields are structured. These fields include:

Opcode (7 bits): Identifies the type of instruction.
funct3 (3 bits): Specifies the operation within the instruction type.
funct7 (7 bits, only for R-type): Further refines the operation.
Register Fields (rd, rs1, rs2): Specify the registers involved.
Immediate (various sizes): Represents constants used in operations.
Each instruction type is designed for specific operations.

1. R-type (Register Type)
Used for: Arithmetic and logical operations involving registers.
Fields:
Field	Bits	Description
funct7	7	Defines the operation (e.g., addition vs. subtraction).
rs2	5	Second source register.
rs1	5	First source register.
funct3	3	Additional operation information.
rd	5	Destination register.
opcode	7	Instruction category.
Example: add a0, a1, a2
Adds a1 and a2, storing the result in a0.
Binary Encoding:
funct7   | rs2  | rs1  | funct3 | rd   | opcode  
0000000  | 00110 | 00101 | 000   | 00100 | 0110011  
2. I-type (Immediate Type)
Used for: Immediate operations, loads, and jumps.
Fields:
Field	Bits	Description
imm[11:0]	12	Signed immediate value.
rs1	5	Source register.
funct3	3	Operation type.
rd	5	Destination register.
opcode	7	Instruction category.
Example: addi a0, a1, 10
Adds 10 to a1, storing the result in a0.
Binary Encoding:
imm[11:0] | rs1  | funct3 | rd   | opcode  
000000001010 | 00001 | 000   | 00010 | 0010011  
3. S-type (Store Type)
Used for: Storing values into memory.
Fields:
Field	Bits	Description
imm[11:5]	7	Upper part of immediate value.
rs2	5	Data register.
rs1	5	Base address register.
funct3	3	Operation type.
imm[4:0]	5	Lower part of immediate value.
opcode	7	Instruction category.
Example: sw a0, 16(sp)
Stores a0 at memory address sp + 16.
Binary Encoding:
imm[11:5] | rs2  | rs1  | funct3 | imm[4:0] | opcode  
0000010   | 00010 | 00010 | 010   | 00000    | 0100011  
4. B-type (Branch Type)
Used for: Conditional branching (e.g., beq, bne).
Fields:
Field	Bits	Description
imm[12	10:5]	7
rs2	5	Second register for comparison.
rs1	5	First register for comparison.
funct3	3	Defines branch type (e.g., equal, not equal).
imm[4:1	11]	5
opcode	7	Instruction category.
Example: beq a0, a1, 16
If a0 == a1, jump to PC + 16.
Binary Encoding:
imm[12|10:5] | rs2  | rs1  | funct3 | imm[4:1|11] | opcode  
000000 | 00001 | 00000 | 000   | 00000 | 1100011  
5. U-type (Upper Immediate Type)
Used for: Loading large immediate values (lui, auipc).
Fields:
Field	Bits	Description
imm[31:12]	20	Immediate value (upper bits).
rd	5	Destination register.
opcode	7	Instruction category.
Example: lui a0, 0x12345
Loads 0x12345000 into a0.
Binary Encoding:
imm[31:12] | rd   | opcode  
00010010001101000101 | 00010 | 0110111  
6. J-type (Jump Type)
Used for: Jumping to an address (jal).
Fields:
Field	Bits	Description
imm[20	10:1	11
rd	5	Destination register (stores return address).
opcode	7	Instruction category.
Example: jal ra, 1024
Jumps to address PC + 1024 and stores return address in ra.
Binary Encoding:
imm[20|10:1|11|19:12] | rd   | opcode  
000000100000 | 00001 | 1101111  
Summary of Instruction Types
Type	Purpose	Example
R-type	Register operations	add a0, a1, a2
I-type	Immediate operations, loads	addi a0, a1, 10
S-type	Store operations	sw a0, 16(sp)
B-type	Conditional branching	beq a0, a1, 16
U-type	Large immediate values	lui a0, 0x12345
J-type	Unconditional jumps	jal ra, 1024
Each type is designed for a specific set of operations, making RISC-V simple yet powerful.

Task 4

Task 4.1

![image](https://github.com/user-attachments/assets/7dec12b7-7833-40db-9f77-3cf520dd7a70)

Task 4.2 

![image](https://github.com/user-attachments/assets/728c36b7-0ca3-46c1-a53c-461b9969ce6e)

Task 4.3 

![image](https://github.com/user-attachments/assets/7d43af82-fabc-4f81-bbf6-c8c984acf57c)

Task 4.4 

![image](https://github.com/user-attachments/assets/26decc1d-239a-4e78-8902-77f5a44747c1)

Task 4.5

![image](https://github.com/user-attachments/assets/80847b4e-c6ca-447e-816c-8a4dc3d1e43b)
