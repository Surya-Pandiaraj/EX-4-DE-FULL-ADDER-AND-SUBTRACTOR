### NAME: SURYA P <br>
### REG NO: 212224230280

# EX 4 : FULL ADDER AND SUBTRACTOR

## AIM :

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

## EQUIPMENTS REQUIRED :

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

## FULL ADDER AND FULL SUBTRACTOR 

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

## TRUTH TABLE 

FULL ADDER

![exp 4 (TT1)](https://github.com/user-attachments/assets/7e3238ee-17c1-40a5-9062-815f21116d11)

FULL SUBRACTOR

![exp 2 (TT2)](https://github.com/user-attachments/assets/af33a305-cb2d-43ae-a806-8722875788e6)

## PROCEDURE :

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram


## PROGRAM :

```

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 

Developed by: Surya P

RegisterNumber: 212224230280

*/


FULL ADDER
module fulladder(a,b,cin,sum,carry);

input a,b,cin;

output sum,carry;

assign sum=( (a ^ b)^cin);

assign carry= ( (a & b)| ( cin &(a ^ b )));

endmodule

FULL SUBRACTOR
module fs(a,b,bin,difference,borrow);

input a,b,bin;

output difference,borrow;

assign difference= ( (a ^ b)^bin);

assign borrow= ( ( a & b)| ( bin & ((a ^ b ))));

endmodule

```

## RTL SCHEMATIC : 

FULL ADDER

![image](https://github.com/user-attachments/assets/a7041465-1bed-4142-88cf-9fd8bfa09321)

FULL SUBRACTOR

![image](https://github.com/user-attachments/assets/14296602-923e-4373-a58b-d80744a77660)

## OUTPUT TIMING WAVEFORM : 

FULL ADDER

![image](https://github.com/user-attachments/assets/e40ed1d0-d900-4e67-8fe1-c2f3fdb0de10)

FULL SUBRACTOR

![image](https://github.com/user-attachments/assets/69c57a04-0a43-4e4f-8aca-0e1beb49ff42)

## RESULT :

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.
