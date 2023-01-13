# EXPERIMENT-04-IMPLEMENTATIOM-OF-COMBINATIONAL-LOGIC-USING-UNIVERSAL-GATES
 
## AIM:

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

1.Create a project with required entities.  
2.Create a module along with respective file name.  
3.Run the respective programs for the given boolean equations.  
4.Run the module and get the respective RTL outputs.  
5.Create university program(VWF) for getting timing diagram.  
6.Give the respective inputs for timing diagram and obtain the results.  

## PROGRAM :

Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programming. 

Developed by: MIDHUN AZHAHU RAJA P 
RegisterNumber: 22008311

### USING NAND OPERATION :
```
module fourexp(A,B,C,D,F);  
input A,B,C,D;  
output F;  
wire P,Q,R;  
assign P = C&(~B)&(~A);  
assign Q = D&(~C)&(~A);  
assign R = (~C)&B&(~A);  
assign F = (~P&~Q&~R);  
endmodule  
```
### USING NOR OPERATION :
```
module fourexp(A,B,C,D,F);  
input A,B,C,D;  
output F;  
wire P,Q,R,S;  
assign P = C&(~B)&A;  
assign Q = D&(~C)&A;  
assign R = C&(~B)&A;  
assign S = ~(P|Q|R);  
assign F = ~S;  
endmodule  
```
## OUTPUT :

### FOR NAND :

### RTL REALIZATION FOR NAND GATE :

![Screenshot_20230109_081312](https://user-images.githubusercontent.com/118054670/211349014-38b8eb2a-bfa2-4051-83c6-4daa8ccc7bc5.png)

### TIMING DIAGRAM : 

![Screenshot_20230109_082920](https://user-images.githubusercontent.com/118054670/211349341-9250c3ad-8585-49b0-8872-4f82b6663c1e.png)

### TRUTH TABLE :

![192572747-c981f4d7-4efe-45a1-b530-e5f3a4f701c0](https://user-images.githubusercontent.com/118054670/211349891-b36be638-bf19-49da-aa7c-f506e4936413.png)

### FOR NOR :

### RTL REALIZATION FOR NOR GATE :

![Screenshot_20230109_084110](https://user-images.githubusercontent.com/118054670/211350221-3f9289e0-a139-4882-85a5-0fcede81f521.png)

### TIMING DIAGRAM : 

![Screenshot_20230109_084919](https://user-images.githubusercontent.com/118054670/211350361-7b2a93a1-f71a-4ff1-99d3-47330e61ef26.png)

### TRUTH TABLE :

![193070747-02a10b19-554b-4d48-996b-deb3daf2c284](https://user-images.githubusercontent.com/118054670/211350552-665332a9-85a6-4b81-8627-18e8a2ba57bd.png)

## RESULT :
Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
