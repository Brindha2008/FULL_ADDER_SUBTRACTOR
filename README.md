
DATE:-25/11/2025

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
FUL ADDER:-
```
module full_adder (
    input  wire a, b, cin,   // Inputs
    output wire sum, carry   // Outputs
);

    // Logic equations
    assign sum   = a ^ b ^ cin;                  // XOR for sum
    assign carry = (a & b) | (b & cin) | (a & cin); // Majority function for carry

endmodule
```
FULL SUB:-
```
module full_subtractor (
    input  wire a, b, bin,       // Inputs
    output wire diff, borrow     // Outputs
);

    // Logic equations
    assign diff   = a ^ b ^ bin;                  // Difference
    assign borrow = (~a & b) | (~(a ^ b) & bin);  // Borrow logic

endmodule
```
Deveploed by:Brindha A R

Register no:25013493


**RTL Schematic**
FULL ADDER :-
<img width="1183" height="678" alt="Screenshot 2025-11-25 214402" src="https://github.com/user-attachments/assets/ca3b999a-2f8e-43bc-9816-53c45182b839" />
FULL SUB:-
<img width="1183" height="547" alt="Screenshot 2025-11-25 214755" src="https://github.com/user-attachments/assets/815f545e-2077-4f2f-8e61-cd2d21ce7f95" />



**Output Timing Waveform**
FULL ADDER:-
<img width="1542" height="273" alt="Screenshot 2025-11-25 214419" src="https://github.com/user-attachments/assets/abe206dd-5114-4d50-9113-5b5b0f41cf29" />
FULL SUB:-
<img width="1576" height="351" alt="Screenshot 2025-11-25 214810" src="https://github.com/user-attachments/assets/948f7fca-1ebb-482d-ba17-5b7741909470" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.


.
.
.
.

.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.
.


.
.
.
.
.
.

.
.
.
.

.
.
.
.
.
.


.
.
.
.
.
.
.
.
.
.

.
.
.
.
.
.
.
.

.
.
.
.
.
.
.
.

.

.

.



..
...
.
.
.
.
.
.
.
.




