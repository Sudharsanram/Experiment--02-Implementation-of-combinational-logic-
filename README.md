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
 

## Logic Diagram
## Procedure
## Program:

```

module DE_02(A,B,C,D,F1);
input A,B,C,D;
output F1;
wire x1,x2,x3,x4,x5;
assign x1=(~A)&(~B)&(~C)&(~D);
assign x2=(A)&(~C)&(~D);
assign x3=(~B)&(C)&(~D);
assign x4=(~A)&(B)&(C)&(D);
assign x5=(B)&(~C)&(D);
assign F1= x1 | x2 | x3 | x4  |x5;
endmodule

```
/*
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
# Developed by: SUDHARSAN RAM M
# RegisterNumber:  212222110048
*/
## Output:

![Screenshot 2023-08-26 094944](https://github.com/Sudharsanram/Experiment--02-Implementation-of-combinational-logic-/assets/119393980/de2e9e3f-6a9c-4e4c-8b7f-6a5889265057)
![de02 ](https://github.com/Sudharsanram/Experiment--02-Implementation-of-combinational-logic-/assets/119393980/462ac9cc-7510-4fa9-ab8d-e2355c53830f)


## RTL

![image](https://github.com/Sudharsanram/Experiment--02-Implementation-of-combinational-logic-/assets/119393980/250474a6-747e-40cb-be3b-4d0c5473adb6)



## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
