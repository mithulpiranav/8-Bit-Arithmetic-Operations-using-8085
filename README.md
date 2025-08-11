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

<img width="1545" height="911" alt="image" src="https://github.com/user-attachments/assets/47a90a36-f4d0-4b1a-988e-4ce6133740e7" />

### Output:

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

<img width="1540" height="851" alt="image" src="https://github.com/user-attachments/assets/f76ac548-66f1-42dd-8690-fdb6603d8c2e" />


### Output:

<img width="296" height="550" alt="image" src="https://github.com/user-attachments/assets/a51571c3-46e4-41a3-b6fe-7034b3544bc3" />


<img width="292" height="575" alt="image" src="https://github.com/user-attachments/assets/2161aa9a-dd99-4b32-9210-511b17b841ff" />

### For Multiplication:
1.	Load the first number from memory location 4200H into register A.
2.	Load the second number from memory location 4201H into register B.
3.	Multiply A and B using repeated addition.
4.	Store the result in memory locations 4300H and 4301H (if required for higher bits).

### Program:

### Output:

### For Division:
1.	Load the dividend from memory location 4200H into register A.
2.	Load the divisor from memory location 4201H into register B.
3.	Perform division using repeated subtraction.
4.	Store the quotient in 4300H and remainder in 4301H.

### Program:

### Output:

## Result:
The 8-bit arithmetic operations using the 8085 microprocessor have been successfully executed and verified using memory access for input and output.

