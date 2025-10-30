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

![image](https://github.com/user-attachments/assets/b09e7332-958e-4e84-9f53-7affd2357d9c)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/user-attachments/assets/ca8e58aa-8470-42ed-8d58-e2f5effe7f02)

**Figure -1 FULL SUBTRACTOR**

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**
FULL ADDER

![image](https://github.com/user-attachments/assets/4d112be1-6902-42f6-a80f-d6ffa1814c34)

FULL SUBTRACTOR

![image](https://github.com/user-attachments/assets/affd2a74-295b-48dc-b7c5-3e2de75db7d3)




**Procedure**

Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram.


**Program:**
```
Program to design a full adder and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by:h mohammed irfan
RegisterNumber: 25006317
```
**Full Adder**

```
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
```
**Full Subtractor**

```
module full_subtractor(diff, borrow, a, b, bin);
  output diff;
  output borrow;
  input a;
  input b;
  input bin;
  assign diff = a ^ b ^ bin;
  assign borrow = (~a & b) | (~(a ^ b) & bin);
endmodule

```

**RTL Schematic**
**Full Adder**

![image](https://github.com/user-attachments/assets/993f7ad7-9159-46a4-8769-48a7a7b701f3)

**Full Subtractor**
![image](https://github.com/user-attachments/assets/5d7d76ec-1151-443f-adde-8d9412dd223b)


**Output Timing Waveform**
**Full Adder**

![image](https://github.com/user-attachments/assets/3bc3543a-312f-4602-b767-8f7462e5c877)

**Full Subtractor**
![image](https://github.com/user-attachments/assets/0d64db0f-5039-49e4-89e9-02676e122512)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



