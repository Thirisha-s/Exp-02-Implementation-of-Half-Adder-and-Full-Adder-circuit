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
### Program
Developed by: s.thirisha
RegisterNumber:  212222230160
# half adder:
```
module halfadder(a,b,s,c);
input a,b;
output s,c;
xor (s,a,b);
and (c,a,b);
endmodule
```
# full adder:
```
module fulladder(a,b,ci,s,co);
input a,b,ci;
output s,co;
wire d,e,f;
xor (d,a,b);
xor (s,d,ci);
and (f,a,b);
or (co,e,f);
endmodule
```
### Output:
### RTL:
# half adder:
![Screenshot 2023-03-28 203253](https://user-images.githubusercontent.com/120380280/228281863-61e4a539-83c7-4533-9147-27cc0907d9ce.png)
# full adder
![Screenshot 2023-03-28 203304](https://user-images.githubusercontent.com/120380280/228282005-5af5d457-ef17-4ca3-b6e2-927e3b425e23.png)

### TIMING DIAGRAM:
# half adder:
![Screenshot 2023-03-28 203522](https://user-images.githubusercontent.com/120380280/228282470-c9baee44-896e-4d8c-ae4a-f56bcd56836a.png)
# full adder:
![Screenshot 2023-03-28 203539](https://user-images.githubusercontent.com/120380280/228282564-50a2b6f0-adfc-4664-a177-751da8fdedab.png)

### TRUTH TABLE :
# hald adder:
![Screenshot 2023-03-28 203547](https://user-images.githubusercontent.com/120380280/228282753-06896acf-5fbb-4022-801c-e1a6bc0474a3.png)
# full adder:
![Screenshot 2023-03-28 203555](https://user-images.githubusercontent.com/120380280/228282840-fb15b2fa-f483-49b7-be53-d4a148fab6f2.png)

### Result:
Thus the Implementation of Half Adder and Full Adder circuit are studied and the truth table for different logic gates are verified.
