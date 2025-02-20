# TMR Spiking Neural Network on FPGA (Q8.8 Fixed-Point)

This project implements a **Triple Modular Redundancy (TMR) Spiking Neural Network (SNN)** using the **Leaky Integrate-and-Fire (LIF) neuron model** on an **FPGA (Spartan-3E Starter Kit)**. The implementation uses **Q8.8 fixed-point arithmetic** for efficient hardware computation.

## 📌 Project Overview
- **Triple Modular Redundancy (TMR)** ensures fault tolerance by using three independent neurons and a majority voter.
- **Leaky Integrate-and-Fire (LIF) Neuron Model** is implemented with fixed-point arithmetic.
- **Fixed-Point Arithmetic (Q8.8 Format)** is used for efficient computation instead of floating-point operations.
- **Designed for FPGA (Xilinx ISE Design Suite)** to be synthesized and tested on hardware.

## 🗂️ File Structure

| File Name                | Description |
|--------------------------|-------------|
| `fixed_point_q8_8.v`      | Performs Q8.8 fixed-point arithmetic (addition, subtraction, multiplication). |
| `lif_neuron_q8_8.v`      | Implements the LIF neuron model using fixed-point arithmetic. |
| `tmr_lif_neuron.v`       | Implements Triple Modular Redundancy (TMR) for fault-tolerant neural computation. |
| `tmr_lif_neuron_tb.v`    | Testbench for verifying the TMR LIF neuron functionality. |

## 🛠️ Setup Instructions
### 1️⃣ Prerequisites
- **Xilinx ISE Design Suite** (For synthesis and simulation)
- **Spartan-3E Starter Kit** (Target FPGA hardware)

### 2️⃣ Running the Simulation
1. Open **Xilinx ISE Design Suite**.
2. Create a new project and add the **Verilog source files**.
3. Set `tmr_lif_neuron_tb.v` as the **top-level simulation module**.
4. Run the **behavioral simulation** to verify the neuron model and TMR logic.

### 3️⃣ FPGA Synthesis & Implementation
1. Assign appropriate **FPGA constraints (UCF file)**.
2. Synthesize the design and generate the **bitstream (.bit file)**.
3. Upload the bitstream to the **Spartan-3E FPGA**.

## ✅ Verification & Testing
- The testbench **`tmr_lif_neuron_tb.v`** provides test cases for fault-tolerant neural processing.
- Ensure correct **spike generation** and **membrane potential updates**.
- Validate majority voting under **fault scenarios**.
