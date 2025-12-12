# SERIAL-IN-SERIAL-OUT-SHIFTREGISTER

**AIM:**

To implement  SISO Shift Register using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**SISO shift Register**

A Serial-In Serial-Out shift register is a sequential logic circuit that allows data to be shifted in and out one bit at a time in a serial manner. It consists of a cascade of flip-flops connected in series, forming a chain. The input data is applied to the first flip-flop in the chain, and as the clock pulses, the data propagates through the flip-flops, ultimately appearing at the output.

The logic circuit provided below demonstrates a serial-in serial-out (SISO) shift register. It comprises four D flip-flops that are interconnected in a sequential manner. These flip-flops operate synchronously with one another, as they all receive the same clock signal.

<img width="1082" height="311" alt="Screenshot 2025-12-11 000617" src="https://github.com/user-attachments/assets/7edcb953-89a1-45da-9432-3363c919dfec" />

Figure 01 4 Bit SISO Register

The synchronous nature of the flip-flops ensures that the shifting of data occurs in a coordinated manner. When the clock signal rises, the input data is sampled and stored in the first flip-flop. On subsequent clock pulses, the stored data propagates through the flip-flops, moving from one flip-flop to the next.
Each D flip-flop in the circuit has a Data (D) input, a Clock (CLK) input, and an output (Q). The D input represents the data to be loaded into the flip-flop, while the CLK input is connected to the common clock signal. The output (Q) of each flip-flop is connected to the D input of the next flip-flop, forming a cascade.

**Procedure**

1.Create a new Verilog project in Quartus. 


2.Enter and save the SISO shift register code.


3.Compile the program.


4.Apply inputs in the waveform editor and simulate.


5.Observe the timing diagram and verify the data shifting.


**PROGRAM**
```
module LabExercise6(clk, sin, q);
input clk;
input sin;
output [3:0] q;
reg [3:0] q;
always @(posedge clk)
begin
q[0] <= sin;
q[1] <= q[0];
q[2] <= q[1];
q[3] <= q[2];
end
endmodule

Developed by:N.Gowsalya
RegisterNumber:25016458
```

**RTL LOGIC FOR SISO Shift Register**

<img width="1920" height="1080" alt="Screenshot (63)" src="https://github.com/user-attachments/assets/bca37837-4716-4468-9c1a-3cb98e344a31" />


**TIMING DIGRAMS FOR SISO Shift Register**

<img width="1920" height="1080" alt="Screenshot (72)" src="https://github.com/user-attachments/assets/de69be87-7f15-435b-83b0-e700382d65fe" />


**RESULTS**

This Program was excecuted successfully
