# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure



Write the detailed procedure here 


## Program:
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: Mourise jane s 
RegisterNumber: 212222230085 
/*

//Half Subtractor Program:

module HalfSubtractor(A,B,Difference,Borrow);
input A,B;
output Difference,Borrow;
assign Difference = (A ^ B);
assign Borrow = (~A & B);
endmodule

//Full Subtractor Program:

module FullSubtractor(A,B,C,Difference,Borrow);
input A,B,C;
output Difference,Borrow;
assign Difference = (~A &(B ^ C) | (B & C));
assign Borrow = ( A^B^C);
endmodule
*/

## Output:

## Truthtable
### Half subractor:
![233019093-6afe4766-bf66-46c2-98eb-738ef543058a](https://user-images.githubusercontent.com/120081893/233124958-323c013b-a48a-43f1-bda8-41f50777c100.png)

### Full subractor:
![233019115-34b8e1cf-216b-49eb-9231-46ab34090dd8](https://user-images.githubusercontent.com/120081893/233125213-0575b97d-e45e-4c70-84bc-c574470e5569.png)

### Logic Daigram
## Half subracor:
![full subractor](https://user-images.githubusercontent.com/120081893/233128746-cfb9229c-0cce-4705-9337-54f401ad7077.png)
## Full subractor:
![subractor](https://user-images.githubusercontent.com/120081893/233127774-c62d13eb-a9c5-4ba8-a3f4-1d0e1f2ecd06.png)





##  RTL realization
# Half subractor:
![Screenshot 54](https://user-images.githubusercontent.com/120081893/233131534-1fb41182-ecbb-49f3-b2f1-793d703940ef.png)

## Full subractor:
![Screenshot 55](https://user-images.githubusercontent.com/120081893/233131699-696ed7af-a65e-461b-b258-ff2aff6a138c.png)


## Timing diagram 
# Half subractor:
![Screenshot 39](https://user-images.githubusercontent.com/120081893/233137220-27fd3934-d3ac-4a27-915c-bfdab984471c.png)

# Full subractor:
![Screenshot 40](https://user-images.githubusercontent.com/120081893/233137490-d3b0653f-f7b3-4891-8141-db6140af53c9.png)




## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
