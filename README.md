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

/* write all the steps invloved */

**PROGRAM**
module asynchronouscounter ( input clk, // clock input input reset, // asynchronous
 reset output [3:0] q // 4-bit output ); // Internal flip-flop outputs reg [3:0] q_reg;
 endmodule
 /* Program for 4 Bit Ripple Counter and verify its truth table in quartus using Verilog
 programming.
 Developed by:s.vishvabala RegisterNumber:25006451
 RTL LOGIC FOR 4 Bit Ripple Counter
 assign q = q_reg;
 // First flip-flop toggles with clock
 always @(posedge clk or posedge reset) begin
    if (reset)
        q_reg[0] <= 0;
    else
        q_reg[0] <= ~q_reg[0];
 end
 // Each next FF toggles with the previous FF’s output
 always @(posedge q_reg[0] or posedge reset) begin
    if (reset)
        q_reg[1] <= 0;
    else
        q_reg[1] <= ~q_reg[1];
 end
 always @(posedge q_reg[1] or posedge reset) begin
    if (reset)
        q_reg[2] <= 0;
    else
        q_reg[2] <= ~q_reg[2];
 end
 always @(posedge q_reg[2] or posedge reset) begin
    if (reset)
        q_reg[3] <= 0;
    else
        q_reg[3] <= ~q_reg[3];
  end

endmodule
/* Program for 4 Bit Ripple Counter and verify its truth table in quartus using Verilog programming.

 Developed by:GOPIKA.G RegisterNumber:25015795
*/

**RTL LOGIC FOR 4 Bit Ripple Counter**
<img width="467" height="627" alt="image" src="https://github.com/user-attachments/assets/9053f35e-c40d-41e8-9e12-af5e74de5e42" />


**TIMING DIGRAMS FOR 4 Bit Ripple Counter**
<img width="752" height="408" alt="image" src="https://github.com/user-attachments/assets/9cee44c9-e31b-4ee1-b8e7-2fe207c66d84" />

**RESULTS**
 Thus 4-BIT-RIPPLE-COUNTER is verified successfully
