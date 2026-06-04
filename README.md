# 32-bit CORDIC Processor for Cosine and Logarithm Computation

## Overview

This project presents the design, verification, synthesis, and physical implementation of a 32-bit CORDIC (Coordinate Rotation Digital Computer) processor capable of computing cosine and natural logarithm functions. The architecture utilizes the CORDIC algorithm, which relies on iterative shift-add operations instead of hardware multipliers, making it highly suitable for FPGA and ASIC implementations.

The design was developed in Verilog HDL and implemented using the Cadence digital design flow, including NCLaunch for functional verification, Genus for synthesis, and Innovus for physical design.

---

## Key Features

* 32-bit fixed-point implementation
* Dual operating modes:

  * Cosine Computation (Rotation Mode)
  * Natural Logarithm Computation (Hyperbolic Vectoring Mode)
* Multiplier-free architecture using shift-add operations
* Hardware-efficient implementation suitable for DSP applications
* Complete RTL-to-GDSII implementation flow

---

## Design Methodology

### Cosine Calculation

The processor operates in CORDIC rotation mode, where a vector is iteratively rotated toward the target angle using predefined arctangent values. The cosine value is obtained from the final X-coordinate after convergence.

### Logarithm Calculation

For logarithmic computation, the processor operates in hyperbolic vectoring mode. Iterative coordinate transformations are performed using inverse hyperbolic tangent values, and the final accumulated angle corresponds to the logarithmic result.

---

## Tools Used

| Stage                   | Tool                         |
| ----------------------- | ---------------------------- |
| RTL Design              | Verilog HDL                  |
| Functional Verification | Cadence NCLaunch             |
| Logic Synthesis         | Cadence Genus                |
| Physical Design         | Cadence Innovus              |
| Timing Analysis         | Static Timing Analysis (STA) |

---

## Implementation Flow

1. RTL Design and Verification
2. Functional Simulation
3. Logic Synthesis using Cadence Genus
4. Floorplanning
5. Placement Optimization
6. Clock Tree Synthesis
7. Routing
8. DRC and Connectivity Verification
9. Timing Closure
10. Power Analysis
11. Post-Layout Verification

---

## Results

### Synthesis Results

* Positive Timing Slack Achieved
* Total Cell Area: 2780.118 units²
* No Timing Violations

### Physical Design Results

* Successful Floorplanning and Placement
* DRC-Clean Routing
* Positive Setup and Hold Slack
* Successful Clock Tree Synthesis
* Power Integrity Verification Completed

---

## Applications

* FPGA-based DSP Systems
* Software Defined Radio (SDR)
* Embedded Signal Processing
* Real-Time Mathematical Computation
* ASIC Arithmetic Accelerators
* Communication Systems
* ASIC Physical Design
* Memory and Emerging Computing Technologies
