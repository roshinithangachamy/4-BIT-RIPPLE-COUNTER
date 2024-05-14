## EX-12 <p align="center"><b> 4-BIT-RIPPLE-COUNTER </b>    

**DATE:**


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

```
1. Understand the verilog module ripple counter.
2. Use a verilog simulator and write a testbench module to apply clock.
3. Generate clock and reset signal, apply them to the counter module and observe count output.
4. Compile both the counter module and testbench,simulate the design and verify that the counter counts from 0-15
5. Analyse the timing diagram to ensure proper counter behavior.
```

**PROGRAM**

**Developed by: T.ROSHINI**

**RegisterNumber:212223230175**
```
module ripple_counter(
     input wire clk,
	  input wire rst,
	  output reg[3:0] count
	  );
	  
always @(posedge clk or posedge rst)
begin
     if(rst)
	     count <= 4'b0000;
	  else 
	     count <= count + 1;
end 
endmodule 
```
**RTL LOGIC FOR 4 Bit Ripple Counter**

![bit rtl](https://github.com/roshinithangachamy/4-BIT-RIPPLE-COUNTER/assets/147118341/f894ec00-35ff-42aa-91d4-33a3c4f83828)

**TIMING DIGRAMS FOR 4 Bit Ripple Counter**

![4 bit](https://github.com/roshinithangachamy/4-BIT-RIPPLE-COUNTER/assets/147118341/bf1e161f-d49e-4f1c-91d4-bed3185e20cf)

**RESULTS**

thus implement  4 Bit Ripple Counter using verilog and validating their functionality using their functional tables
is done successfully.
