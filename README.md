### Name: Amaljosh Maadhav J
### Roll No: 23014023
# Experiment 03: Implementation of half subtractor and full subtractor circuit
# AIM
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.
#  Equipments Required
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
# Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor and Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)

Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

# Procedure
Connect the supply (+5V) to the circuit

Switch ON the main switch

If the output is 1, then the led glows.

# Program:
## Half Subtractor
module halfsubtractor(input x,y,output b,d);

assign d=x^y;

assign b=~x&y;

endmodule
## Full Subtractor
module fullsubtractor(input x,y,z, output d,b);

assign d=x^y^z;

assign b=~x&(y^z)|y&z;

endmodule



#  RTL realization
## Half Subtractor
![Exp 4 half subtractor RTL realization](https://github.com/amal-2006/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/148410730/5c47bbf1-2a5c-491e-80f5-370396674863)

## Full Subtractor
![Exp 4 full subtractor RTL realization](https://github.com/amal-2006/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/148410730/f7af6f01-56c0-4bd5-98d9-37b2a2f571ce)


# Truthtable
## Half Subtractor
![Exp 4 half subtractor truth table](https://github.com/amal-2006/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/148410730/af8956e9-6319-46ad-b682-2f36ed847872)

## Full Subtractor
![Exp 4 full subtractor truth table](https://github.com/amal-2006/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/148410730/dab6e1b0-1626-4c39-aa65-61f53440cf17)

# Timing diagram 
## Half Subtractor
![Exp 4 half subtractor timing diagram](https://github.com/amal-2006/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/148410730/a15f03e8-1073-4113-b2f8-bb49436f22b5)

## Full Subtractor
![Exp 4 full subtractor timing diagram](https://github.com/amal-2006/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/148410730/852ade89-86ed-40bc-962c-8f713c63baf7)


# Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
