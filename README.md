# NAME: KAVI M S
# REFERENCE NUMBER: 23013458

# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.
# PROCEDURE
1.Use module projname(input,output) to start the Verilog programmming.

2.Assign inputs and outputs using the word input and output respectively.

3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

4.Use each output to represnt onre for differnce and the other for borrow.

5.End the verilog program using keyword endmodule

## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.

![166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a](https://github.com/Kavi45-msk/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/147457752/6336adea-7233-4793-a128-fdb338bcc62f)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

# PROGRAM
```
module project_4_1(a,b,borrow,diff);
input a,b;
output borrow,diff;
assign borrow=~a&b;
assign diff=a^b;
endmodule
```
# RTL REALIZATION
![291255631-24c991b9-2505-4e57-b23a-bc8d29030589](https://github.com/Kavi45-msk/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/147457752/5e672719-40cf-47ce-8ecb-29b83c5fae1a)

# TRUTH TABLE
![291255700-bbe4f57d-e237-4d64-8829-d5f1d8eb7259](https://github.com/Kavi45-msk/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/147457752/b11a9dfc-cc81-4799-9c8f-ad05a0f62db1)

# TIMING DIAGRAM
![291255810-452cb7d7-303b-4e75-8c5e-9c6d9a074c99](https://github.com/Kavi45-msk/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/147457752/fa31fe80-49a5-4616-9ccf-6d4708897632)

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Program:
```
module project_4_2(a,b,bin,borrow,diff);
input a,b,bin;
output diff,borrow;
assign diff=(a^b)^bin;
assign borrow=((~a)&&bin)||(b&&bin)||((~a)&&b);
endmodule
```

##  RTL realization
![291256368-8a12efe3-c86e-4800-a68f-c70a7befe09e](https://github.com/Kavi45-msk/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/147457752/4387c7fe-0d95-4f75-89e2-8ec6200d55c8)

## Truthtable
![291256384-531e58ee-f0b6-4146-b10e-5116dcf5f12f](https://github.com/Kavi45-msk/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/147457752/0b190dfe-0ae3-4cea-8799-63d14fd42175)

## Timing diagram 
![291256418-37e4998a-532a-4fd5-9411-3c5447e13330](https://github.com/Kavi45-msk/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/147457752/ed397c38-b97d-4655-88c0-77c69dba6521)

# RESULT
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
