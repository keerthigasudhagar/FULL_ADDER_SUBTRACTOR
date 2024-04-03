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
```
Full Adder
![315064567-e5e9b28c-8569-4f22-8d9a-f00f3791d592](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/163229129/4e2b370d-ea33-463f-8c2b-f4811a6f050e)
```
```
Full Subtractor
![315065119-a549746d-5b01-4493-af45-09d21f7b1b39](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/163229129/3895abeb-9192-49ca-b3de-a36bb3d7c445)
```
**Procedure**
```
Full adder

1.Open Quartus II and create a new project.

2.Use schematic design entry to draw the full adder circuit.

3.The circuit consists of XOR, AND, and OR gates.

4.Compile the design, verify its functionality through simulation.

5.Implement the design on the target device and program it.

Full subtractor

1.Follow the same steps as for the full adder.

2.Draw the full subtractor circuit using schematic design.
3.The circuit includes XOR, AND, OR gates to perform subtraction.

4.Compile, simulate, implement, and program the design similarly to the full adder.
```

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: keerthika.s RegisterNumber:212223040093
*/
```
module Fulladdsub(a,b,cin,sum,carry,BO,DIFF);
input a,b,cin;
output sum,carry,BO,DIFF;
assign sum=(a^b^cin);
assign carry=(a&b)|(a&cin)|(b&cin);
assign DIFF=(a^b^cin);
assign BO=(~a&b)|(~(a^b)& cin);
endmodule
```
**RTL Schematic**
![313991378-80d06b2e-6dbd-4f67-bf6b-d99f13b77d0c](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/163229129/a61d437c-d261-414d-bac4-6f49a62abb56)

**Output Timing Waveform**
![313991290-0cc2e5bb-12b2-4593-a282-e444ee12875f](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/163229129/8b1b3213-d3c8-4a76-9fe2-71bb6fb66515)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



