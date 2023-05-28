# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
Program:
```
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: Lavanya M

RegisterNumber:  212222110021
*/
HALF ADDER:

module halfadder(A,B,C,S);
input A,B;
output S,C;
xor(S,A,B);
and(C,A,B);
endmodule

FULL ADDER:

module fulladd(A,B,Ci,S,Co);
input A,B,Ci;
output S,Co;
wire D,E,F;
xor(D,A,B);
xor(S,D,Ci);
and(E,Ci,D);
and(F,A,B);
or(Co,E,F);
endmodule
```
Logic symbol & Truthtable
RTL realization

### Output:  
HALF ADDER
![halfadder](https://user-images.githubusercontent.com/120103862/229356243-981ac1ec-a46b-4c67-a1d5-cce1abe0151b.png)

FULL ADDER:
![fulladder](https://user-images.githubusercontent.com/120103862/229356298-fb2f9e3b-1858-4963-b7f9-c0b03b2f7767.png)

###LOGIC GATES:
Logic symbol of Half adder:

![image](https://user-images.githubusercontent.com/120103862/229356774-38037677-e0d0-471f-b346-af600f11842f.png)

Logic symbol of Full adder:

![image](https://user-images.githubusercontent.com/120103862/229356797-d1dc6875-4185-4669-9063-198083953d11.png)


### TIMING DIAGRAM
HALF ADDER:
![halfadder diagram](https://user-images.githubusercontent.com/120103862/229356405-29f8c3ab-88f8-4168-aa69-4c27621d713f.png)

FULL ADDER:
![fulladder diagram](https://user-images.githubusercontent.com/120103862/229356379-3b2fef4a-9983-4bfd-84f3-13a1092798dd.png)

### TRUTH TABLE 

 TRUTH TABLE FOR HALF ADDER:
![image](https://user-images.githubusercontent.com/120103862/229356445-1963a551-7a81-4649-bb70-ba37682a9e48.png)

TRUTH TABLE FOR FULL ADDER:
![image](https://user-images.githubusercontent.com/120103862/229356458-9247a8ae-7079-413d-9984-e3ac54e46c43.png)

### Result:
Thus the half adder and full adder are studied and the truth table for different logic gates are verified.
