# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
## Theory:
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.
## Logic Diagram (using nand gate) and (using nor gate):
![image](https://github.com/JeevaMurthy/Experiment--02-Implementation-of-combinational-logic-/assets/147222117/92390ee1-d19c-4315-a7d0-b585cfaa73df)

![image](https://github.com/JeevaMurthy/Experiment--02-Implementation-of-combinational-logic-/assets/147222117/82b0199f-cb59-469b-ae07-7c4e077383a0)

## Procedure
*Create a project with required entities.
*Create a module along with respective file name.
*Run the respective programs for the given boolean equations.
*Run the module and get the respective RTL outputs.
*Create university program(VWF) for getting timing diagram.
*Give the respective inputs for timing diagram and obtain the results.
## Program:
```
Developed by:JEEVA K
REG NO:212223230090
```
```
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: JEEVA K
RegisterNumber: 23013748
module combinational(a,b,c,d,w,x,y,z,fl,f2);
input a,b,c,d,w,x,y,z;
output fl,f2;
wire g1=((~a)&(~b)&(~c)&(~d)); 
wire g2=((a)&(~c)&(~d));
wire g3=((~b)&(c)&(~d));
wire g4=((~a)&(b)&(c)&(d)); 
wire g5=((b)&(~c)&(d));
assign fl=g1|g2|g3|g4|g5; 
wire g6=((x)&(~y)&(z));
wire g7=((~x)&(~y)&(z));
wire g8=((~w)&(x)&(y)); 
wire g9=((w)&(~x)&(y));
wire g10=((w)&(x)&(y)); 
assign f2=g6|g7|g8|g9|g10;
endmodule
```
## OUTPUT:
## RTL realization of NAND AND NOR gates:
![image](https://github.com/JeevaMurthy/Experiment--02-Implementation-of-combinational-logic-/assets/147222117/6fcee4a7-37c3-404c-bc99-f177c4292cb8)

![image](https://github.com/JeevaMurthy/Experiment--02-Implementation-of-combinational-logic-/assets/147222117/144e837f-3b67-49a9-bcb5-d05a083d3ba4)

## Truthtable of NAND gate:
![image](https://github.com/JeevaMurthy/Experiment--02-Implementation-of-combinational-logic-/assets/147222117/1cc76e14-ca47-4c64-8490-5e67a94dca58)
## Truthtable of NOR gate:
![image](https://github.com/JeevaMurthy/Experiment--02-Implementation-of-combinational-logic-/assets/147222117/80e3ea5d-4627-4866-a4ec-f60ddd455765)

## Timing Diagram:
![image](https://github.com/JeevaMurthy/Experiment--02-Implementation-of-combinational-logic-/assets/147222117/6287881a-2436-463c-9c1b-239b54a97936)

## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
