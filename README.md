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
![WhatsApp Image 2026-03-24 at 8 21 06 PM](https://github.com/user-attachments/assets/8c9998b1-90f4-4d8d-a13e-420651ed1702)

**Procedure**

Write the detailed procedure here

**Program:**
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

module sub(a,b,c,x,y,z,sum,dif,car,bor);
input a,b,c,x,y,z;
output sum,dif,car,bor;
assign sum = a^b^c;
assign car = a&b | a&c | b&c;
assign dif = x^y^z;
assign bor = ~x&z | ~x&y | y&z;
endmodule

```
**RTL Schematic**
<img width="948" height="515" alt="Screenshot 2026-03-18 151240" src="https://github.com/user-attachments/assets/29fa98ae-942e-4281-ae06-f008837abac1" />
<img width="945" height="524" alt="Screenshot 2026-03-18 151349" src="https://github.com/user-attachments/assets/4e9655f9-cfd5-4a2d-98cf-61f0acfb3688" />


**Output Timing Waveform**
<img width="1590" height="839" alt="Screenshot 2026-03-18 151428" src="https://github.com/user-attachments/assets/0eca3c03-8789-401b-8c8b-f42483693cf7" />

**Result:**
<img width="1620" height="859" alt="Screenshot 2026-03-18 151518" src="https://github.com/user-attachments/assets/b95f8966-43a2-4c40-a58f-2bd1cc60bf80" />

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



