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
1. FULL ADDER
![image](https://github.com/user-attachments/assets/27463775-7f9a-4c65-b6cd-48c21f14468d)
2. FULL SUBTRACTER
![image](https://github.com/user-attachments/assets/0b4b69f3-bb5c-4b13-82a6-90c1177fa92e)

**Procedure**
Type the program in Quartus software.

1. Compile and run the program.

2. Generate the RTL schematic and save the logic diagram.

3. Create nodes for inputs and outputs to generate the timing diagram.

4. For different input combinations generate the timing diagram.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/
i) FULL ADDER
module fa(a,b,cin,sum,carry);

input a,b,cin;

output sum,carry;

assign sum=( (a ^ b)^cin);

assign carry= ( (a & b)| ( cin &(a ^ b )));

endmodule

ii)FULL SUBTRACTOR

module fs(a,b,bin,difference,borrow);

input a,b,bin;

output difference,borrow;

assign difference= ( (a ^ b)^bin);

assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));

endmodule

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by: Jayani K

RegisterNumber: 24005008

*/
**RTL Schematic**
i) FULL ADDER
![image](https://github.com/user-attachments/assets/6c7145e6-d657-4536-bfe0-1d0148c60925)
ii) FULL SUBTRACTER
![image](https://github.com/user-attachments/assets/4abe3d8a-12b0-4531-9d2a-eb56ec00d7ce)

**Output Timing Waveform**
i) FULL ADDER
![image](https://github.com/user-attachments/assets/427a3b58-a777-4ea6-aa5a-8764708b7c5f)
ii) FULL SUBTRACTER
![image](https://github.com/user-attachments/assets/1d4ad15a-e60e-442f-badb-dede972a6a6e)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



