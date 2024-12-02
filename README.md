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

 Developed by: Rhudhra phriyamvadha K S
 RegisterNumber: 24900189

Full subtractor:
```
module fullsub(a,b,bin,dif,bor);
 input a,b,bin;
 output dif,bor;
 assign difference=a^b^bin; 
assign borrow=~(a^b)&bin|(~a)&b;
endmodule
```
Full adder:
```
module fulladder(sum, cout, a, b, cin);
    output sum;
    output cout;
    input a;
    input b;
    input cin;
 wire w1,w2,w3;
	 assign w1=a^b;
	 assign w2=a&b;
	 assign w3=w1&cin;
	 assign sum=w1^cin;
	 assign cout=w2|w3;
endmodule
```

**RTL Schematic**
Full subtractor
![Screenshot 2024-11-28 131531](https://github.com/user-attachments/assets/e22cedab-6e0f-45fe-817b-ddcda2ccdffe)

Full adder
![fulladder](https://github.com/user-attachments/assets/66fa3219-2ea3-4f8c-b3f8-148bcb12ae9d)

**Output Timing Waveform**
Full subtractor
![Screenshot 2024-12-02 193104](https://github.com/user-attachments/assets/8266b57e-eb59-438b-b393-f2bf4d0de401)

Full adder
![waveform fulladder](https://github.com/user-attachments/assets/6c3da33a-9a4f-4284-900a-c416277ccea2)


**Result:**

Thus, the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



