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



1. Understand the 4-bit up-counting sequence (0000–1111).

2. Write the Verilog module using a common clock and reset.

3. Compile the code and remove errors.

4. Create a testbench with clock and reset signals.

5. Simulate and verify the count sequence to validate functionality.
/* write all the steps invloved */

**PROGRAM**
<img width="1920" height="1080" alt="synchronous up counter program" src="https://github.com/user-attachments/assets/6df54e98-9c3d-4fb0-9e07-b76386aaf65d" />

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 

Developed by:S Tozer Theophilus RegisterNumber:25016814
*/

**RTL LOGIC UP COUNTER**
<img width="906" height="368" alt="synchronous up counter RTL diagram" src="https://github.com/user-attachments/assets/785e3362-2b10-41ed-a85e-26e6e3678f30" />

**TIMING DIAGRAM FOR IP COUNTER**
<img width="1920" height="1080" alt="synchronous up counter waveform" src="https://github.com/user-attachments/assets/757d56bd-4e92-4651-ad53-9914694f9c72" />

**TRUTH TABLE**

**RESULTS**
The 4-bit synchronous up counter was successfully implemented and simulated. The output count increased sequentially from 0000 to 1111 on each clock pulse, and the results matched the expected up-counting sequence, confirming correct functionality.
