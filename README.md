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
### Program:

```verilog
HALF ADDER

module halfadd(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule 
```
```verilog
FULL ADDER

module fulladd(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule
```
```
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: P.Nevil Joe Ferdin
RegisterNumber: 212222050041 
```

### Output:

### HALF ADDER
#### RTL
![ha rtl ](https://user-images.githubusercontent.com/115524975/231493646-88d2e2fc-4d4a-4c45-8edd-aeb27c83a31f.png)


#### TIMING DIAGRAM
![ha waveform](https://user-images.githubusercontent.com/115524975/231493561-d10bfb09-e920-48bd-b6a7-6fdcdd733cff.png)



#### TRUTH TABLE 
![ha trtab](https://user-images.githubusercontent.com/115524975/231490769-8843bf66-b9c9-4263-8a45-f8b8c12b1c14.png)


### FULL ADDER
#### RTL
![rtl fa](https://user-images.githubusercontent.com/115524975/231496492-c7e0ffdd-9867-412c-bc2d-7d6344fd2511.png)


#### TIMING DIAGRAM
![wave](https://user-images.githubusercontent.com/115524975/231494560-b0783a17-8242-42f3-b681-82e3b7440252.jpeg)




#### TRUTH TABLE 
![fa time](https://user-images.githubusercontent.com/115524975/231496603-26fc62bd-9e77-4af8-a87b-3d4a508bf1a5.png)

### Result:
Thus, a half adder and full adder circuit is designed to verify its truth table in Quartus using Verilog programming.
