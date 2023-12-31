# NAME: PRASHANTH>K
# REGISTER NUMBER:212223230152

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

![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png) 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.

## program
```
module ha(sum,carry,a,b);
output sum,carry;
input a,b;
assign sum=a^b;
assign carry=a&b;
endmodule
```

## RTL 

![image](https://github.com/kannan-nagaraju/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145742755/bd2e465c-08ca-4140-ba6a-6e0a0433fbda)

## TIMING DIAGRAM

![image](https://github.com/kannan-nagaraju/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145742755/fd600a31-f7dc-43c0-88e1-8ab62e68999d)

## TRUTH TABLE


![image](https://github.com/kannan-nagaraju/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145742755/4d8f96d2-dbfc-4659-af27-0e31db87a8e2)




### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.

## program
```
module FULLADDER(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
wire x,p,q,r;
xor(x,b,c);
xor(sum,x,a);
and(p,a,b);
and(q,b,c);
and(r,a,c);
or(carry,p,q,r);
endmodule
```
## RTL
![image](https://github.com/kannan-nagaraju/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145742755/b34705cc-8d48-43be-8d83-e394f3346a2c)

## TIMING DIAGRAM
![image](https://github.com/kannan-nagaraju/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145742755/a34b09ca-9646-47e5-834d-e9e603964b07)

## TRUTH TABLE
![image](https://github.com/kannan-nagaraju/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/145742755/290a19aa-5b07-4008-8f1a-9ee8ee18d58a)


### Result:
Thus the given logic functions are implemented and their operations are verified using verilog programming
