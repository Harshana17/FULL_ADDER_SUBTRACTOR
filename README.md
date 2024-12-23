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

**FULL ADDER**

![WhatsApp Image 2024-12-23 at 23 21 37_d36aa54c](https://github.com/user-attachments/assets/9dfa44d2-efa2-4360-8843-330ee38f8ad5)

**FULL SUBTRACTOR**

![WhatsApp Image 2024-12-23 at 23 22 21_9f9b1d6d](https://github.com/user-attachments/assets/b583babd-b283-4900-8c39-c83503156eb3)



**Procedure**

**Full adder:**

1.Open Quartus II and create a new project.

2.Use schematic design entry to draw the full adder circuit.

3.The circuit consists of XOR,AND,and OR gates.

4.Compile the design,verify its functionality through simulation.

5.Implement the design on the target device and program it.

**Full Subtractor:**

1.Follow the same steps as for the full adder.

2.Draw the full subtractor circuit using schematic design.

3.The circuit includes XOR,AND,OR gates to perform subtraction.

4.Compile,simulate,implement and program the design similarly to the full adder.

**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by: Harshana M V

RegisterNumber:24002128

i)FULL ADDER

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



**RTL**

**FULL ADDER**

![WhatsApp Image 2024-12-23 at 23 08 54_56275bc9](https://github.com/user-attachments/assets/9416bf6e-6126-400b-b10e-03fe692a03d1)

**FULL SUBTRACTOR**

![WhatsApp Image 2024-12-23 at 23 09 19_522ea495](https://github.com/user-attachments/assets/d7d3f710-b7b8-45ae-b2cc-15b18e689ba6)


**Output**

**FULL ADDER**

![WhatsApp Image 2024-12-23 at 23 14 04_a9a5c50d](https://github.com/user-attachments/assets/3936caf9-91ce-4c50-94ec-c7155f877a71)

**FULL SUBTRACTOR**

![WhatsApp Image 2024-12-23 at 23 16 04_f0e333a5](https://github.com/user-attachments/assets/3ae24e89-b042-4394-a0c1-433915fb911e)



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



