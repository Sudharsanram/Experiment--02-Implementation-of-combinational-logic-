# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
Hardware – PCs, Cyclone II , USB flasher Software – Quartus prime Theory Introduction Logic gates are the basic building blocks of any digital system. Logic gates are electronic circuits having one or more than one input and only one output. The relationship between the input and the output is based on a certain logic. Based on this, logic gates are named as

AND gate OR gate NOT gate NAND gate NOR gate Ex-OR gate Ex-NOR gate

AND gate The AND gate is an electronic circuit that gives a high output (1) only if all its inputs are high. A dot (.) is used to show the AND operation i.e. A.B or can be written as AB
Y= A.B

OR gate The OR gate is an electronic circuit that gives a high output (1) if one or more of its inputs are high. A plus (+) is used to show the OR operation.
Y= A+B

NOT gate The NOT gate is an electronic circuit that produces an inverted version of the input at its output. It is also known as an inverter. If the input variable is A, the inverted output is known as NOT A. This is also shown as A' or A with a bar over the top, as shown at the outputs.
Y= A'

NAND gate This is a NOT-AND gate which is equal to an AND gate followed by a NOT gate. The outputs of all NAND gates are high if any of the inputs are low. The symbol is an AND gate with a small circle on the output. The small circle represents inversion.
Y= (AB)’

NOR gate This is a NOT-OR gate which is equal to an OR gate followed by a NOT gate. The outputs of all NOR gates are low if any of the inputs are high. The symbol is an OR gate with a small circle on the output. The small circle represents inversion.
Y= (A+B)’

Ex-OR gate The 'Exclusive-OR' gate is a circuit which will give a high output if either, but not both of its two inputs are high. An encircled plus sign (⊕) is used to show the Ex-OR operation.
Y= A⊕B

Ex-NOR gate The 'Exclusive-NOR' gate circuit does the opposite to the EX-OR gate. It will give a low output if either, but not both of its two inputs are high. The symbol is an EX-OR gate with a small circle on the output. The small circle represents inversion.
Y= A⊕B
 

## Procedure:
Connect the supply (+5V) to the circuit Switch ON the main switch Press the switches for inputs “A” and “B”. The switch is ON state when 1 is pressed. The switch is OFF state when 0 is pressed. If the output is 1, then the bulb glows. Check all the gates following the same procedure.

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
