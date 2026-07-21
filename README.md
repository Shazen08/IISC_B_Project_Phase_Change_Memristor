# MoTe2 Phase-Change Memristor Modeling & Logic Circuit Simulation

This repository contains the complete physical modeling, mathematical validation, Verilog-A implementation, and SPICE-level logic gate performance simulations for a **MoTe2 Phase-Change Memristor**. 

The project bridges low-level device physics (Arrhenius-based thermal-electric switching) with practical circuit applications, comparing the power efficiency of memristor-based logic against traditional CMOS resistor-based logic.

---

## Repository Structure

```text
├── models/
│   ├── Memristor_Python_Code.py       # Standalone Python I-V and state-variable simulation script
│   ├── Memristor_Verilog_Python_Superimposed.py # Superimposed comparison script
│   └── A_Mem_Code_Alpha.va            # Core Verilog-A behavioral model (includes anti-windup mechanics)
├── netlists/
│   ├── A_Mem_Code_Alpha.in            # Transient SPICE testbench for single-device hysteresis verification
│   ├── A_Mem_Code_1_NOT.in            # Pure memristor NOT gate circuit netlist
│   ├── A_Mem_Code_2_NAND.in           # Pure memristor NAND gate circuit netlist
│   ├── A_Mem_Code_3_NOR.in            # Pure memristor NOR gate circuit netlist
│   ├── A_Mem_Code_4_AND.in            # Cascaded memristor AND gate circuit netlist
│   └── A_Mem_Code_5_OR.in             # Cascaded memristor OR gate circuit netlist
├── data/
│   ├── A_Mem_Code_Alpha_I_vs_V_Verilog_Data.txt # Raw ASCII export mapping SPICE simulation outputs
│   ├── A_Mem_Code_1_NOT_Avg_Power.measure.raw0  # Power measurement log for NOT gate
│   ├── A_Mem_Code_2_NAND_Avg_Power.measure.raw1 # Power measurement log for NAND gate
│   ├── A_Mem_Code_3_NOR_Avg_Power.measure.raw2  # Power measurement log for NOR gate
│   ├── A_Mem_Code_4_AND_Avg_Power.measure.raw3  # Power measurement log for AND gate
│   └── A_Mem_Code_5_OR_Avg_Power.measure.raw4   # Power measurement log for OR gate
└── simulations/
    ├── Memristor_Python_Code.png              # Standalone Python model output plot
    ├── Memristor_Verilog_Python_Superimposed.png # High-resolution comparative validation plot
    ├── A_Mem_Code_Alpha_Sim.png               # Single-device transient waveform simulation output
    ├── A_Mem_Code_1_NOT_Sim.png               # NOT gate transient simulation output
    ├── A_Mem_Code_2_NAND_Sim.png              # NAND gate transient simulation output
    ├── A_Mem_Code_3_NOR_Sim.png               # NOR gate transient simulation output
    ├── A_Mem_Code_4_AND_Sim.png               # AND gate transient simulation output
    └── A_Mem_Code_5_OR_Sim.png                # OR gate transient simulation output
