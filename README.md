# 32-bit Floating Point Multiplier

## Overview
This project implements a **32-bit Floating Point Multiplier** based on the **IEEE 754 single-precision format** using **Verilog HDL**. The design follows standard digital design principles and is verified using **Universal Verification Methodology (UVM)**.

## Features
- Supports IEEE 754 single-precision format
- Implements normalization, rounding, and exception handling
- Designed for FPGA/ASIC implementation
- Verified using UVM methodology
- Synthesis and layout generation using OpenROAD tools

## Prerequisites
To work with this project, you need the following tools installed:

- **Verilog Simulator** (e.g., ModelSim, QuestaSim, or Xilinx Vivado)
- **Synthesis Tools** (e.g., Synopsys Design Compiler, Yosys)
- **UVM Verification Framework**
- **OpenROAD for Physical Design**

## Project Structure
```
├── src/                     # Source Verilog files
│   ├── fp_multiplier.v      # 32-bit Floating Point Multiplier
│   ├── normalizer.v         # Normalization module
│   ├── rounding.v           # Rounding logic
│   ├── exceptions.v         # Exception handling
│   ├── testbench/           # Testbench and UVM verification
│
├── synthesis/               # Synthesis scripts and results
├── layout/                  # GDS-II generation using OpenROAD
├── docs/                    # Documentation and reports
├── README.md                # Project overview
```

## Design Methodology
1. **IEEE 754 Format Handling**:
   - Extract sign, exponent, and mantissa.
   - Perform multiplication on mantissas.
   - Adjust exponent and normalize the result.
   - Apply rounding and handle exceptions.
   
2. **Verification Using UVM**:
   - Testbench with constrained-random stimulus.
   - Functional coverage and assertions.
   - Regression testing for accuracy.

3. **Synthesis & Layout**:
   - RTL synthesis using Yosys/Synopsys DC.
   - Floorplanning and routing using OpenROAD.
   - Timing analysis (STA) to ensure correct performance.

## Running the Simulation
To run the testbench:
```
cd src/testbench
vsim -do run.do   # For ModelSim/QuestaSim
```

For UVM-based verification:
```
make verify   # Run UVM tests
```

## Generating GDS-II
To perform physical design using OpenROAD:
```
cd layout
make gds
```

## Results & Performance
- **Clock Frequency**: TBD (based on synthesis results)
- **Area Utilization**: TBD
- **Power Consumption**: TBD

## Future Enhancements
- Support for fused multiply-add (FMA)
- Optimized pipelining for higher throughput
- Enhanced exception handling

## References
- IEEE 754 Floating Point Standard
- OpenROAD Documentation
- UVM Verification Methodology

## License
This project is licensed under the MIT License.

---
##Author
##NAGARAJ KANNI


