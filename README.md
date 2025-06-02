### NAME : GOKUL S
### REG NO : 212224230075

### SYNCHRONOUS UP COUNTER

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

![Screenshot 2025-05-06 094114](https://github.com/user-attachments/assets/ea475180-78bd-4fc7-8f99-ca1903b87b34)


**PROGRAM**
```
module exp11(out,clk,rstn);
input clk,rstn;
output reg [3:0]out;
always @ (posedge clk)
begin
if(!rstn)
 out<=0;
else 
 out <= out+1;
end
endmodule

```

Developed by: GOKUL S  RegisterNumber:212224230075
*/

**RTL LOGIC UP COUNTER**

![Screenshot 2025-05-06 093620](https://github.com/user-attachments/assets/353c76d8-d6b0-4844-b6ff-13ee2c551c6a)


**TIMING DIAGRAM FOR IP COUNTER**

![Screenshot 2025-05-06 093804](https://github.com/user-attachments/assets/f2a57af0-29d0-4f42-8698-d8e790fb3508)

**TRUTH TABLE**

![Screenshot 2025-05-06 093841](https://github.com/user-attachments/assets/88a54504-8cea-41c6-839d-fc6e57a6d236)

**RESULTS**

Implementation of 4 bit synchronous up counter and validate functionality.
