# 8-Bit-Arithmetic-Operations-using-8085
## Aim:
To perform 8-bit arithmetic operations such as addition, subtraction, multiplication, and division using the 8085 microprocessor.

## Apparatus Required:
•	Laptop with internet connection

## Algorithm:

### For Addition (With Carry Consideration):
1.	Load the first number from memory location 4200H into register A.
2.	Load the second number from memory location 4201H into register B.
3.	Add the contents of registers A and B.
4.	If carry is generated, store carry in 4301H.
5.	Store the sum in memory location 4300H.
   
### Program:

      CMC
      LDA 4200H
      MOV B,A
      LDA 4201H
      ADD B
      STA 4300H
      JC STORE_CARRY
      HLT
      STORE_CARRY: MVI A,01H
      STA 4301H
      HLT


### Output:

<img width="1545" height="911" alt="image" src="https://github.com/user-attachments/assets/47a90a36-f4d0-4b1a-988e-4ce6133740e7" />


<img width="305" height="491" alt="image" src="https://github.com/user-attachments/assets/304fab6f-84eb-4de0-8d2e-bb399a3e93bb" />

<img width="304" height="518" alt="image" src="https://github.com/user-attachments/assets/33072a85-f5bb-473a-9f7f-365c52a83222" />

### For Subtraction (Considering Greater Number):
1.	Load the first number from memory location 4200H into register A.
2.	Load the second number from memory location 4201H into register B.
3.	Compare A and B.
4.	If A < B, swap the values of A and B to ensure positive result.
5.	Subtract the content of B from A.
6.	Store the result in memory location 4300H.

### Program:

      LDA 4200H
      MOV C,A
      LDA 4201H
      CMP C
      JC SWAP
      SWAP:
      MOV B,A
      MOV A,C
      SUB B
      STA 4300H
      HLT

### Output:

<img width="1546" height="888" alt="image" src="https://github.com/user-attachments/assets/1600fc2d-6a85-4ec0-8eec-c3c76f77ffbe" />


<img width="305" height="443" alt="image" src="https://github.com/user-attachments/assets/d568cf4c-3494-4511-a231-a632fc4e73fc" />

<img width="309" height="428" alt="image" src="https://github.com/user-attachments/assets/392d36d8-c269-4569-8aa0-c56a85544586" />

### For Multiplication:
1.	Load the first number from memory location 4200H into register A.
2.	Load the second number from memory location 4201H into register B.
3.	Multiply A and B using repeated addition.
4.	Store the result in memory locations 4300H and 4301H (if required for higher bits).

### Program:

      LDA 4200H
      MOV C,A
      LDA 4201H
      MOV B,A
      MVI A,00H
      LOOP:ADD C
      DCR B
      JNZ LOOP
      STA 4300H
      HLT


### Output:

<img width="1525" height="786" alt="image" src="https://github.com/user-attachments/assets/4815e88b-f25d-4180-950d-0a1b82847a22" />


<img width="302" height="466" alt="image" src="https://github.com/user-attachments/assets/73f94387-114e-4db3-8704-f3b029c96580" />

<img width="306" height="430" alt="image" src="https://github.com/user-attachments/assets/496177b6-53ed-48e4-818c-91615d4d40de" />

### For Division:
1.	Load the dividend from memory location 4200H into register A.
2.	Load the divisor from memory location 4201H into register B.
3.	Perform division using repeated subtraction.
4.	Store the quotient in 4300H and remainder in 4301H.

### Program:

      LDA 4200H
      MOV C,A
      LDA 4201H
      MOV B, A
      MVI A, 00H
      LOOP: CMP B
      JC END 
      SUB B
      INR A
      JMP LOOP
      END: STA 4300H
      MOV A, C
      STA 4301H
      HLT


### Output:

<img width="1558" height="1085" alt="image" src="https://github.com/user-attachments/assets/ad57b74c-fb3e-4ade-813b-b60d8b62391f" />



<img width="298" height="488" alt="image" src="https://github.com/user-attachments/assets/79389f3a-a354-40b5-bd18-f3171d0a74b9" />

<img width="300" height="490" alt="image" src="https://github.com/user-attachments/assets/a2cee633-be25-46bb-8740-3bce656f4460" />

## Result:
The 8-bit arithmetic operations using the 8085 microprocessor have been successfully executed and verified using memory access for input and output.

