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
![EX 4 1](https://github.com/user-attachments/assets/e29d4cfa-ac40-4af2-96f7-3957b0a6a9bd)

![EX4 2](https://github.com/user-attachments/assets/18a4507a-639b-4bda-99ba-36fcc9d73d77)



**Procedure**

Write the detailed procedure here

**Program:**
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:GOKUL V E 
RegisterNumber:24002047
```
```
 module fulladdsub(a,b,cin,bin,sum,carry,difference,borrow); 
input a,b,cin,bin; output sum,carry,difference,borrow; 
assign sum=a^b^cin; 
assign carry=(a^b)&cin|a&b;
 assign difference=a^b^bin; 
assign borrow=~(a^b)&bin|(~a)&b
```

**RTL Schematic**

![EX 4 3](https://github.com/user-attachments/assets/7b171502-a1fa-430d-bbe9-6822a0293ddc)


**Output Timing Waveform**
![EX4 4](https://github.com/user-attachments/assets/e24f2785-25a4-411c-9ca0-4ce596b975a8)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



