# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder **

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Truthtable**
<img width="902" height="434" alt="Screenshot 2026-03-24 215234" src="https://github.com/user-attachments/assets/808211ea-345c-404f-b43d-ac1363b491db" />


**Procedure**
1. Type the program in Quartus software.

2. Compile and run the program.

3. Generate the RTL schematic and save the logic diagram.

4. Create nodes for inputs and outputs to generate the timing diagram.

5. For different input combinations generate the timing diagram.

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

```
**RTL Schematic**
<img width="1280" height="800" alt="image" src="https://github.com/user-attachments/assets/0ead8ea8-c2b3-4d8d-b632-ac4be77d92df" />

**Output Timing Waveform**
<img width="1590" height="839" alt="Screenshot 2026-03-18 151428" src="https://github.com/user-attachments/assets/0eca3c03-8789-401b-8c8b-f42483693cf7" />

**Result:**
<img width="1620" height="859" alt="Screenshot 2026-03-18 151518" src="https://github.com/user-attachments/assets/b95f8966-43a2-4c40-a58f-2bd1cc60bf80" />

Thus the Full Adder  circuit are designed and the truth tables is verified using Quartus software.



