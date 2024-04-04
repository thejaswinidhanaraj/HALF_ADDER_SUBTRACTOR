# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**

![half adder](https://github.com/thejaswinidhanaraj/HALF_ADDER_SUBTRACTOR/assets/148514511/187203b3-5700-4f2c-a4e5-da2e30e4ecd4)


![half subractor](https://github.com/thejaswinidhanaraj/HALF_ADDER_SUBTRACTOR/assets/148514511/9b1cf812-237b-4b0a-b3b8-edd08ef53acd)

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by:D.Thejaswini
RegisterNumber:212223110059
```
module HALF_ADDSUB(a,b,sum,carry,D,Bo);
input a,b;
output sum,carry,D,Bo; // Outputs sum and carry for half adder:Outputs difference D,Borrow Bo for half subtractor
xor(sum,a,b);
and(cary,a,b);
wire abar;
not(abar,a);
xor(D,a,b);
and(Bo,abar,b);
endmodule
```
*/

**RTL Schematic**

![WhatsApp Image 2024-04-04 at 14 03 08_13299faa](https://github.com/thejaswinidhanaraj/HALF_ADDER_SUBTRACTOR/assets/148514511/457deb3c-b52a-43aa-81f9-6bfa964c1f96)

**Output/TIMING Waveform**

![WhatsApp Image 2024-04-04 at 14 03 21_d8ec3ea9](https://github.com/thejaswinidhanaraj/HALF_ADDER_SUBTRACTOR/assets/148514511/8fca48db-4448-43d0-bba9-b20de253577f)


**Result:**

Thus the half adder and half subtractor circuit was designed and verified its truth table in Quartus using Verilog programming.
