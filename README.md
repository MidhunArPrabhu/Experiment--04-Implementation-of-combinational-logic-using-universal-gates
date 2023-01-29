# EXPERIMENT-04
# IMPLEMENTATIOM-OF-COMBINATIONAL-LOGIC-USING-UNIVERSAL-GATES
 
## AIM :

To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog 
programming.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate  
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate  
## EQUIPMENTS REQUIRED :
## Hardware – PCs, Cyclone II , USB flasher  
## Software – Quartus prime 


## THEORY : 

Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output. 

## USING NAND GATES : 

NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

## USING NOR GATES :

NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

## PROCEDURE :
```
1.Create a project with required entities.  
2.Create a module along with respective file name.  
3.Run the respective programs for the given boolean equations.  
4.Run the module and get the respective RTL outputs.  
5.Create university program(VWF) for getting timing diagram.  
6.Give the respective inputs for timing diagram and obtain the results.  
```
## PROGRAM :
```python
Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programming. 

Developed by: MIDHUN AZHAHU RAJA P 
RegisterNumber: 22008311
```
### USING NAND OPERATION :
```python
module nandcomb(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R;
assign P=(~(~C & B & A));
assign Q=(~(~D & C & A));
assign R=(~(C & ~B & A));
assign F=~(P & Q & R);
endmodule
```
### USING NOR OPERATION :
```python
module orcomb(A,B,C,D,F);
input A,B,C,D;
output F;
wire P,Q,R,S;
assign P = (C & ~B & A);
assign Q = (D & ~C & A);
assign R = (C & ~B & A);
assign S = (~(P | Q | R));
assign F = (~s);
endmodule 
```
## OUTPUT :

### FOR NAND :

### RTL REALIZATION FOR NAND GATE :

![nandrtl](https://user-images.githubusercontent.com/118054670/215305686-10a4175d-458e-4d24-9f75-d23d71d00c69.png)

### TIMING DIAGRAM : 

![nandtime](https://user-images.githubusercontent.com/118054670/215305694-03cf20a1-2de2-4bbf-9f9c-091c08911b72.png)

### TRUTH TABLE :

![nandtable](https://user-images.githubusercontent.com/118054670/215305702-b45f909f-9800-412d-87a4-d051baa2ec5e.png)


### FOR NOR :

### RTL REALIZATION FOR NOR GATE :

![orrtl](https://user-images.githubusercontent.com/118054670/215305706-512ce5e1-2a24-4e36-80d0-2fa8035d1628.png)


### TIMING DIAGRAM : 

![oryime](https://user-images.githubusercontent.com/118054670/215305727-4ea13787-0f88-4f0b-bb10-fe594c404b64.png)


### TRUTH TABLE :

![ortable](https://user-images.githubusercontent.com/118054670/215305733-d7ab0a67-ee09-49ed-ba11-9cd538cb4726.png)


## RESULT :

Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
