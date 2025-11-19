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


Full adder


<img width="278" height="181" alt="images" src="https://github.com/user-attachments/assets/9f9fb024-3460-4b96-b12d-51d5c9c1af84" />


Full subtractor


<img width="255" height="198" alt="images (1)" src="https://github.com/user-attachments/assets/e953fc83-6dac-47f0-a8dc-2d7445b18ad2" />


**Procedure**

Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram.
















**Program:**


Full adder

module fulladd(a,b,c,sum,carry);

input a,b,c;

output sum,carry;

assign sum =(a^b^c);

assign carry=(a&b)|(b&c)|(c&a);

endmodule

Full subtractor

module fullsub(a,b,c,D,B);

input a,b,c;

output D,B;

assign D=(a^b^c);

assign B=(~a&c)|(b&c)|(~a&b);

endmodule

**RTL Schematic**

Full adder
<img width="1920" height="1080" alt="Screenshot (98)" src="https://github.com/user-attachments/assets/1b893b04-5723-48f1-87ee-1b0d060690b1" />
Full subtractor
<img width="1920" height="1080" alt="Screenshot (101)" src="https://github.com/user-attachments/assets/e1c9a5d0-9747-4434-9482-ff6d62fd3a3a" />


**Output Timing Waveform**
Full adder
<img width="1920" height="1080" alt="Screenshot (99)" src="https://github.com/user-attachments/assets/ba4bbc10-74a5-4178-b65e-4851fe89467d" />
Full subtractor
<img width="1920" height="1080" alt="Screenshot (102)" src="https://github.com/user-attachments/assets/85bef9e1-8277-4a6e-bad6-9c157b5506b9" />



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



