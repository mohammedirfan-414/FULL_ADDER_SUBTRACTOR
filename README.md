# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

<img width="566" height="512" alt="image" src="https://github.com/user-attachments/assets/4c0c13a8-aeb8-4d53-9837-58ca407006b4" />

**FULL SUBRACTOR**

<img width="572" height="516" alt="image" src="https://github.com/user-attachments/assets/2aa1fb99-9e21-4753-b2bb-e43175e32fd4" />


**Procedure**

Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram


**Program:**

Program to design a full adder and full subtractor circuit and verify its truth table in quartus using Verilog programming. 

**FULL ADDER**

module exp4(df,bo,a,b,bin);
output df;
output bo;
input a;
input b;
input bin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign df=w1^bin;
assign bo=w2|w3;
endmodule

**FULL SUBRACTOR**

module full_subtractor(diff, borrow, a, b, bin);
  output diff;
  output borrow;
  input a;
  input b;
  input bin;
  assign diff = a ^ b ^ bin;
  assign borrow = (~a & b) | (~(a ^ b) & bin);
endmodule 


**RTL Schematic**

FULL ADDER 
<img width="1177" height="744" alt="image" src="https://github.com/user-attachments/assets/4208d47a-aaa7-49b6-ab8a-547cd19fef8d" />

FULL SBRACTOR

<img width="1351" height="542" alt="image" src="https://github.com/user-attachments/assets/e1da0629-a45b-446a-97f8-1a70c30eb8d8" />


**Output Timing Waveform**
FULL ADDER
<img width="1920" height="1201" alt="image" src="https://github.com/user-attachments/assets/b8302d08-fdf7-4358-80b4-b97e3d2b39d0" />

FULL SUBRACTOR
<img width="1921" height="1201" alt="image" src="https://github.com/user-attachments/assets/d3a4e58d-a778-49ae-bc0f-a48c5a21228b" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



