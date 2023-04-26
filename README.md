# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
/* Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.
*/
## Using NOR gates
/*
Using NOR gates NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'
*/

## Logic Diagram
## Procedure
1.Create a project with required entities.
2.Create a module along with respective file name.
3.Run the respective programs for the given boolean equations.
4.Run the module and get the respective RTL outputs.
5.Create university program(VWF) for getting timing diagram.
## Program:
```python
/*
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by:shaik sameer basha 
RegisterNumber:212222240093
*/
## For F1:
module cl (a,b,c,d,f1);
input a,b,c,d;
output f1;
assign f1 = (a&b&~c)|(~a&b&d)|(~b&~d);
endmodule
## For F2:
module cl (w,x,y,z,f2);
input w,x,y,z;
output f2;
assign f2 = (x&y)|(w&y)|(~y&z);
endmodule
```
## RTL realization

## Output:
## RTL
## For F1:
![f1](https://user-images.githubusercontent.com/118707756/234546182-7eea8d3d-c0ac-4ed9-ae3f-6fc46d7988e5.png)
## For F2:
![f2](https://user-images.githubusercontent.com/118707756/234546546-05c029ea-6949-40f3-88ea-c1dadd1e5ec6.png)
## Timing Diagram
## For F1:
![f1t](https://user-images.githubusercontent.com/118707756/234546778-47b9b3ef-cfcd-4e7c-9686-1a858bd55b8b.png)

## For F2:
![f2t](https://user-images.githubusercontent.com/118707756/234546860-c513a979-f5ad-4c1d-879f-a773944a5ae7.png)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
