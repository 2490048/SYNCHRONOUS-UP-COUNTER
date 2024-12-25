### SYNCHRONOUS-UP-COUNTER

**AIM:**

To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 bit synchronous UP Counter**

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.


**PROGRAM**

module ex11(out,clk,rst);

input clk,rst;

output reg [3:0]out;

always @ (posedge clk)

begin

if(rst)

![{C001841F-171C-436B-AE9F-6E7359402D8F}](https://github.com/user-attachments/assets/afd07b44-d959-4bff-8693-336b373c16c1)

else

![{6F3E0F39-8148-4F7B-80FE-E7A8280487AC}](https://github.com/user-attachments/assets/c34e14ee-9d2b-4b5a-9489-eab4062fe999)


end

endmodule

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 

Developed by:RAHUL RP RegisterNumber:24900488
*/

**RTL LOGIC UP COUNTER**

![{E35D6BD7-DA6A-4783-87FC-24A241CAF029}](https://github.com/user-attachments/assets/17fd6547-615f-4430-9c35-a41ac3cd4ee8)


**TIMING DIAGRAM FOR IP COUNTER**

![{A38942B5-9C07-4DF0-B19F-41B7A14BEBFA}](https://github.com/user-attachments/assets/3b42c877-c281-4978-b17e-97120cf6b3eb)


**TRUTH TABLE**

![{0B5E5857-02FB-45FF-A46E-1544578062EE}](https://github.com/user-attachments/assets/fecda2c4-69e7-43a6-89ec-b7d9daed84f2)


**RESULTS**

Hence implemented 4 bit synchronous up counter and validate functionality.
