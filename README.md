# SERIAL-IN-SERIAL-OUT-SHIFTREGISTER
## Name:Nishalini R
## Reg No: 212224040222
**AIM:**

To implement  SISO Shift Register using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**SISO shift Register**

A Serial-In Serial-Out shift register is a sequential logic circuit that allows data to be shifted in and out one bit at a time in a serial manner. It consists of a cascade of flip-flops connected in series, forming a chain. The input data is applied to the first flip-flop in the chain, and as the clock pulses, the data propagates through the flip-flops, ultimately appearing at the output.

The logic circuit provided below demonstrates a serial-in serial-out (SISO) shift register. It comprises four D flip-flops that are interconnected in a sequential manner. These flip-flops operate synchronously with one another, as they all receive the same clock signal.

![image](https://github.com/naavaneetha/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/154305477/e81c4072-37f9-46c6-8145-566764b74c3a)

Figure 01 4 Bit SISO Register

The synchronous nature of the flip-flops ensures that the shifting of data occurs in a coordinated manner. When the clock signal rises, the input data is sampled and stored in the first flip-flop. On subsequent clock pulses, the stored data propagates through the flip-flops, moving from one flip-flop to the next.
Each D flip-flop in the circuit has a Data (D) input, a Clock (CLK) input, and an output (Q). The D input represents the data to be loaded into the flip-flop, while the CLK input is connected to the common clock signal. The output (Q) of each flip-flop is connected to the D input of the next flip-flop, forming a cascade.

**Procedure**

/* write all the steps invloved */

**PROGRAM**
```
module exp10(clk,sin,q);
input clk;
input sin;
output [3:0] q;
reg [3:0] q;
always @(posedge clk)
begin 
q[0] <=sin;
q[1] <=q[0];
q[2] <=q[1];
q[3] <=q[2];
end 
endmodule
```


**RTL LOGIC FOR SISO Shift Register**


![Screenshot 2025-05-14 154114](https://github.com/user-attachments/assets/0646bed9-e68c-4f9f-836c-b711ad4ec1e5)


** WAVEFORM**


![Screenshot 2025-05-14 154137](https://github.com/user-attachments/assets/28e35b2b-95b8-42cb-9f55-2b31f19de284)

**RESULTS**
Implementation of the  SISO Shift Register using verilog and validating their functionality using their functional tables can been done successfully.
