# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

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

**Truthtable**

FULL ADDER :
    
  <img width="740" height="619" alt="Screenshot 2025-12-17 185821" src="https://github.com/user-attachments/assets/3403431c-a652-4446-9982-b31327ee7390" />

FULL SUBTRACTER :

   <img width="738" height="394" alt="Screenshot 2025-12-17 185842" src="https://github.com/user-attachments/assets/22a31cf8-517f-469c-b960-dab1cce5d78d" />



**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.


**Program:**

FULL ADDER:
   
    module fa(a,b,cin,sum,carry);
  
    input a,b,cin;
  
    output sum,carry;
  
    assign sum=( (a ^ b)^cin);
  
    assign carry= ( (a & b)| ( cin &(a ^ b )));
  
    endmodule

FULL SUBTRACTER:
   
    module fs(a,b,bin,difference,borrow);

    input a,b,bin;

    output difference,borrow;

    assign difference= ( (a ^ b)^bin);

    assign borrow= ( ( a & b)| ( bin & ((a ^ b ))));

    endmodule
 
 Developed by: MONISH . R
 RegisterNumber: 25017815


**RTL Schematic**

   <img width="1020" height="511" alt="Screenshot 2025-12-17 185959" src="https://github.com/user-attachments/assets/c43bb3d6-7640-4e62-a12f-2d99c6911279" />

   

   <img width="1019" height="519" alt="Screenshot 2025-12-17 190019" src="https://github.com/user-attachments/assets/ba1ae893-dc40-4d93-8409-714ee3e02864" />


**Output Timing Waveform**

   

<img width="1021" height="508" alt="Screenshot 2025-12-17 190051" src="https://github.com/user-attachments/assets/3b57d11b-ac99-496e-845f-c57a96e1ecaf" />




<img width="1028" height="513" alt="Screenshot 2025-12-17 190113" src="https://github.com/user-attachments/assets/1ae7dce4-5d86-415b-976c-600204f014ac" />


   
**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



