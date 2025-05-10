# 4-BIT-RIPPLE-COUNTER

**AIM:**

To implement  4 Bit Ripple Counter using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 Bit Ripple Counter**

A binary ripple counter consists of a series connection of complementing flip-flops (T or JK type), with the output of each flip-flop connected to the Clock Pulse input of the next higher-order flip-flop. The flip-flop holding the least significant bit receives the incoming count pulses. The diagram of a 4-bit binary ripple counter is shown in Fig. below.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/cb4b74d4-31ab-4359-95d0-d22e67daba13)

In timing diagram Q0 is changing as soon as the negative edge of clock pulse is encountered, Q1 is changing when negative edge of Q0 is encountered(because Q0 is like clock pulse for second flip flop) and so on.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/a573a7d6-014e-4e54-93e6-e2ac9530960b)

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/85e1958a-2fc1-49bb-9a9f-d58ccbf3663c)

**Procedure**

Step 1: Initialize the Counter Initialize the 4-bit counter with all bits set to 0 (0000).

Step 2: Receive Clock Pulse Receive a clock pulse (CLK).

Step 3: Check Clock Pulse If the clock pulse is 0, go to step 8.

Step 4: Toggle LSB (Q0) Toggle the least significant bit (Q0).

Step 5: Check Q0 If Q0 is 1, go to step 6.

Step 6: Toggle Q1 Toggle the next bit (Q1).

Step 7: Repeat for Q2 and Q3 Repeat steps 5-6 for Q2 and Q3.

Step 8: Update Counter Outputs Update the counter outputs (Q3, Q2, Q1, Q0).

Step 9: Repeat Repeat steps 2-8 for each clock pulse.

**PROGRAM**
```
module exp12(out,clk,rst);
input clk,rst;
output reg [3:0]out;
always @ (posedge clk)
begin
   if(rst)
     out<=0;
   else 
     out <= out+1;
end
endmodule
```
 Developed by: JYOTSHANA S R
 
 RegisterNumber:212224230111

**RTL LOGIC FOR 4 Bit Ripple Counter**
![image](https://github.com/user-attachments/assets/10be80c6-a19c-4e3f-8793-a6cd62b335cf)

**TIMING DIGRAMS FOR 4 Bit Ripple Counter**

![image](https://github.com/user-attachments/assets/4ee13fb0-4a8c-495e-9e4c-9d348b590e72)

**RESULTS**
Thus implementing 4 Bit Ripple Counter using Verilog and validating their functionality using their functional tables is done successfully.
