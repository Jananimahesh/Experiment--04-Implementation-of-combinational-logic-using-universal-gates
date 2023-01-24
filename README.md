# Experiment--04-Implementation-of-combinational-logic-using-universal-gates
Implementation of combinational logic using universal-gates
 
## AIM:
To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output. 

## Using NAND gates
NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

## Logic Diagram

Using NOR gates
NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

## Logic Diagram
## Procedure
1.create a project with required entities
2.create a module along with respective file name.
3.Run the respective programs for the given boolean equations.
4.Run the module and get RTL outputs
5.Create university program(VWF)for getting timing diagram
6.Give the respective inputs for timing diagram and obtain the results

## Program:
/*
Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programming.
Developed by: janani.m
RegisterNumber:  22006734

FOR NAND GATE 
module combo1(A,B,C,D,F);
input A,B,C,D;
output F;
wire p,q,r;
assign p=(~C & B & A);
assign q=(~D & C & ~A);
assign r=(C & ~B & A );
assign F=(~(~p & ~q & ~r));
endmodule

FOR NOR GATE
module combo2(a,b,c,d,f);
input a,b,c,d;
output f;
assign p=( c & ~b & a );
assign q=( d & ~c & a );
assign r=( c & ~b & a );
assign f=((( p | q | r)));
endmodule

OUTPUT

## RTL realization
using NAND gate

![image](https://user-images.githubusercontent.com/119432417/214346301-ad793416-36a3-4ef9-8c6c-a5d6ebfc68de.png)

using NOR gate

![image](https://user-images.githubusercontent.com/119432417/214346565-20811321-6980-4e57-af4d-2d1e1cd1a438.png)


## Timing Diagram
using NAND gate

![image](https://user-images.githubusercontent.com/119432417/214346951-85b22dec-f632-4998-a57c-21294ff4c942.png)

using NOR gate

![image](https://user-images.githubusercontent.com/119432417/214347203-d2394866-19f9-4781-b539-95151d5d8432.png)

TRUTH TABLE
Using NAND gate 

![image](https://user-images.githubusercontent.com/119432417/214347603-3b0a543e-081e-4539-8ca9-334c30080e64.png)

using NOR gate

![image](https://user-images.githubusercontent.com/119432417/214348321-8a45f2ac-3cdb-4abc-9db8-a6c548e13434.png)



## Result:
Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
