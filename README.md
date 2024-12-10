# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**


![386250654-4576f86c-95df-4a5c-9dd2-699bd622b5c7](https://github.com/user-attachments/assets/f0973134-901c-4a42-be9f-ab56b1dc088b)


![386250695-df2b7631-6624-4b57-9c8a-7b7b89a81b0f](https://github.com/user-attachments/assets/1e1bff8f-0c3e-40e3-bcad-4d423cce141f)

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

```
module ex03(a,b,cy, sm, df,bo);
input a,b; output sm,cy, df, bo;
xor(sm,a,b);
and(cy,a,b);
xor(df,a,b);
and (bo,~a,b);
endmodule
```
Developed by:thillaiajay.l RegisterNumber:24008308
**RTL Schematic**
![386250964-86a715c6-a548-41d1-afa7-3210ed0cae53](https://github.com/user-attachments/assets/6e882d84-2b44-4f45-95bd-dd6e29b90251)

**Output/TIMING Waveform**
![386251042-be1be902-afab-4364-846b-6bf56c31f2cd](https://github.com/user-attachments/assets/c4317415-bd4e-4b64-b7cc-cd73963ab0e9)

**Result:**
Thus the Half Adder and Half Subtractor circuits are designed and the truth tables is verified using Quartus software.
