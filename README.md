## NAME:M.V.Vamsidhar Reddy
## reg: 212224040205
To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

    module boolean(a,b,c,d,w,x,y,z,f1,f2);
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
    and(s,w,y);
    and(t,x,y);
    and(u,ydash,z);
    or(f1,p,q,r);
    or(f2,s,t,u);
    endmodule

**output**

**RTL realization**
<img width="1918" height="1140" alt="boolean RTL" src="https://github.com/user-attachments/assets/f8840e03-4a73-47a0-ab5d-0ec500a6aa5b" />


**University Timing Diagram**

<img width="1918" height="1132" alt="RTL2" src="https://github.com/user-attachments/assets/4b53c6a4-1942-4d6a-aef7-8fc7e43c5459" />


**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.
