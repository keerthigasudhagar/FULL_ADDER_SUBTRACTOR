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

full adder:
![328084690-e0fff7d1-a2f7-4fa0-b9c4-1a49aee2be8f](https://github.com/keerthigasudhagar/FULL_ADDER_SUBTRACTOR/assets/163229129/c1ce60b0-e681-4410-a17d-6e75c2750d79)


**Full subtractor:**
![328084783-826f852d-ba60-4cd5-8e91-fd30cf327e8b](https://github.com/keerthigasudhagar/FULL_ADDER_SUBTRACTOR/assets/163229129/e41c6f6e-99ef-4e56-9544-3406e91d04ce)

**Procedure**


Write the detailed procedure here
```
**Full Adder:**
1.Open Quartus II and create a new project.
2.Use schematic design entry to draw the full adder circuit. 
3.The circuit consists of XOR, AND, and OR gates. 
4.Compile the design, verify its functionality through simulation. 
5.Implement the design on the target device and program it.

**Full Subtractor:** 
1.Follow the same steps as for the full adder. 
2.Draw the full subtractor circuit using schematic design. 
3.The circuit includes XOR, AND, OR gates to perform subtraction. 
4.Compile, simulate, implement, and program the design similarly to the full adder.
```
**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/
```
module fulladdsub(a,b,c,sum,carry,BO,DIFF);
input a,b,c;
output sum,carry,BO,DIFF;
assign sum=a^b^c;
assign carry= a&b | a&c | b&c;
wire a0;
not (a0,a);
assign BO= b&c | a0&c | a0&b;
assign DIFF=a^b^c;
endmodule



Developed by: keerthika.s
RegisterNumber: 212223040093
```

**RTL Schematic**
![328085106-99cb12ac-0a5a-4fb9-b02c-d5a25572e54d](https://github.com/keerthigasudhagar/FULL_ADDER_SUBTRACTOR/assets/163229129/4a38135e-c336-42c7-bfa1-7869fd2dd2e9)


**Output Timing Waveform**

![328085178-f07e90dc-cbcd-4dee-865d-87c12d8347c5](https://github.com/keerthigasudhagar/FULL_ADDER_SUBTRACTOR/assets/163229129/f1b6da80-4248-4e8a-a712-28c237f001f9)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



