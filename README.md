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
 Connect the supply (+5V) to the circuit Switch ON the main switch Press the switches for inputs “A” and “B”. The switch is ON state when 1 is pressed. The switch is OFF state when 0 is pressed. If the output is 1, then the bulb glows. Check all the gates following the same procedure. 


## Program:

/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:  keerthana jayasri
RegisterNumber: 212222110019 

HALF SUBTRACTOR:
module HalfSub(a,b,difference,borrow);
input a,b;
output difference,borrow;
assign difference=(a^b);
assign borrow=(~a&b);
endmodule
FULL SUBTRACTOR:
module FullSub(a,b,c,difference,borrow);
input a,b,c;
output difference,borrow;
assign borrow=(~a&(b^c)|(b&c));
assign difference=(a^b^c);
endmodule

logic gates:

![image](https://github.com/keerthanajayasri/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/121163440/a8fa9f15-5afb-48f7-92c3-75085f33247f)


## Truthtable

![image](https://github.com/keerthanajayasri/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/121163440/848c1eae-bf8b-415c-93d3-7bae3f18eb55)
FULL SUBTRACTOR:


![image](https://github.com/keerthanajayasri/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/121163440/bda6a442-2051-4ebb-b5a2-cdf77a8ca367)

##  RTL realization  
![image](https://github.com/keerthanajayasri/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/121163440/76bde491-a326-464f-9919-e6ddb815f04b)

FULL SUBTRACTOR:



![image](https://github.com/keerthanajayasri/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/121163440/3fb8a9e5-fde2-47e7-9046-30d6ab4771dc)


## Timing diagram 

![image](https://github.com/keerthanajayasri/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/121163440/b6ded3a2-7ece-4d08-b195-ecae3896070a)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
