### EX02 - BOOLEAN_FUNCTION_MINIMIZATION

## AIM:

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

## Equipment Required:

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

## Theory

## Logic Diagram

## Procedure

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


## Program:

Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 
```
Developed by:  Bharathganesh S
RegisterNumber: 212222230022
```

```
module booleanfunction(a,b,c,d,w,x,y,z,f1,f2);
input a,b,c,d,w,x,y,z;
output f1,f2;
wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u;
not(adash,a);
not(bdash,b);
not(cdash,c);
not(ddash,d);
not(ydash,y);
and(p,bdash,ddash);
and(q,adash,b,d);
and(r,a,b,cdash);
or(f1,p,q,r);
and(s,ydash,z);
and(t,x,y);
and(u,w,y);
or(f2,s,t,u);
endmodule

```
## Output:
## RTL realization

![image](https://github.com/user-attachments/assets/e6d385e0-e0bb-4985-b041-a04939114e8f)

## Truth table

![image](https://github.com/user-attachments/assets/041a8c1d-4c67-4f90-966d-a673c7c2082c)

![image](https://github.com/user-attachments/assets/3b0fd628-41ae-44fe-8697-a60cd4aca7e8)


## Timing Diagram
![image](https://github.com/user-attachments/assets/f8fe5349-55c1-42ce-8956-48d5dae512da)


## Result:

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

