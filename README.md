# TMR LIF Neuron on FPGA  

This project implements a **Triple Modular Redundancy (TMR)**-based **Leaky Integrate-and-Fire (LIF) neuron** on an FPGA. The design is written in **Verilog** and uses **Q8.8 fixed-point arithmetic** for efficient computations. The implementation is targeted for the **Spartan-3E Starter Kit** using **Xilinx ISE Design Suite**.

---

## 🚀 **Project Overview**
- **Hardware:** Spartan-3E Starter Kit  
- **Neuron Model:** Leaky Integrate-and-Fire (LIF)  
- **Fault Tolerance:** Triple Modular Redundancy (TMR)  
- **Computation Format:** Q8.8 Fixed-Point Arithmetic  
- **Language:** Verilog HDL  
- **Simulation & Synthesis:** Xilinx ISE Design Suite  

---

## 📂 **File Structure**
```
📂 TMR_LIF_Neuron
 ├── src/
 │   ├── tmr_lif_neuron.v      # TMR-based LIF neuron module
 │   ├── lif_neuron_q8_8.v     # Individual LIF neuron implementation
 │   ├── fixed_point_q8_8.v    # Fixed-point arithmetic functions
 ├── testbench/
 │   ├── tmr_lif_neuron_tb.v   # Testbench for simulation
 │   ├── waveforms.do          # ISim waveform script (if needed)
 ├── docs/
 │   ├── README.md             # Project documentation
 │   ├── Q8.8_format_explained.pdf  # Explanation of Q8.8 arithmetic
 └── README.md
```

---

## 🛠 **Setup & Usage**
### **1️⃣ Prerequisites**
- **Xilinx ISE Design Suite (for simulation & synthesis)**
- **Spartan-3E Starter Kit (for FPGA implementation)**

### **2️⃣ Cloning the Repository**
```bash
git clone https://github.com/yourusername/TMR_LIF_Neuron.git
cd TMR_LIF_Neuron
```

---

## 🔬 **Simulation on Xilinx ISE (ISim)**
1. Open **Xilinx ISE Design Suite**
2. Create a **New Project** and select **Spartan-3E Starter Kit**
3. Add Verilog source files from `src/`
4. Add testbench files from `testbench/`
5. Set `tmr_lif_neuron_tb.v` as the **Top Module**
6. Select **Behavioral Simulation**
7. Click **Simulate Behavioral Model**
8. View results in **ISim Waveform Viewer**

---

## 🏗 **Synthesis & FPGA Implementation**
1. Open **Xilinx ISE Design Suite**
2. Select **Synthesize - XST**
3. Click **Implement Design**
4. Click **Generate Programming File**
5. Connect the **Spartan-3E Starter Kit** via JTAG
6. Open **iMPACT** and load the generated `.bit` file
7. Program the FPGA and observe outputs

---

## 🧪 **Testbench**
The testbench (`tmr_lif_neuron_tb.v`) validates:
✔ Correct spike generation  
✔ Stable membrane potential computation  
✔ Robust fault tolerance under bit-flips or deviations  

To run the testbench:
```bash
vsim work.tmr_lif_neuron_tb
run -all
```
Or directly simulate in **ISim** using the provided steps.

---

## 📊 **Results**
The testbench ensures:
✔ Correct majority voting for neuron membrane potential  
✔ Stable behavior under injected faults  
✔ Correct spike output based on thresholding  

---
