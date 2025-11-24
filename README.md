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

**Procedure**

Write the detailed procedure here

**Program:**
full adder

module fa(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
xor g1(sum,a,b,c);
assign carry=((a&b)|(b&c)|(c&a));
endmodule 

full subractor

module fs(a,b,c,diff,borr);
input a,b,c;
output diff,borr;
xor g1(diff,a,b,c);
assign borr=((~a&b)|(b&c)|(~c&a));
endmodule
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by: Srikanth K
RegisterNumber: 25017937
*/

**RTL Schematic**
<img width="1280" height="681" alt="image" src="https://github.com/user-attachments/assets/b7434d70-ea30-4a77-9416-84919e9bebc0" />

<img width="1280" height="679" alt="image" src="https://github.com/user-attachments/assets/1d6aa5e7-6ee9-45f8-b8fe-82e11a8d9e14" />


**Output Timing Waveform**
<img width="1280" height="678" alt="image" src="https://github.com/user-attachments/assets/f8cbeaf2-f565-40e0-8c72-c7a9a0eab2a5" />
<img width="1280" height="683" alt="image" src="https://github.com/user-attachments/assets/974306f3-2ff3-413f-8143-69b1f49b519b" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



