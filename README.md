# 4-bit SISO and SIPO Shift Register Design using Cadence Virtuoso

## Overview
This repository contains the design and simulation files for 4-bit **Serial-In Serial-Out (SISO)** and **Serial-In Parallel-Out (SIPO)** shift registers, implemented using **Cadence Virtuoso**. The project includes schematic designs, layout implementations, and both pre- and post-simulation results for the shift register configurations.

## Files
- **DFF_Schematic_Sim_AvgPower_Delay_Screenshots/** – Contains schematics, simulation results, average power calculations, and delay analyses for D Flip-Flops.
- **SISO_Schematic_Sim_AvgPower_Delay_Screenshots/** – Includes schematics, simulation results, power, and delay analyses for the 4-bit SISO shift register.
- **SIPO_Schematic_Sim_AvgPower_Delay_Screenshots/** – Contains schematics, simulation results, power, and delay analyses for the 4-bit SIPO shift register.
- **SISO_SIPO_CadenceVirtuoso_Folder/** – Cadence Virtuoso project files for both shift registers.
- ***`SISO_SIPO_CadenceVirtuoso_Folder.zip`*** – Zipped version of the project folder.

## Requirements

- ***Cadence Virtuoso*** – For schematic capture and layout design.
- ***Spectre Simulator*** – For running simulations and analyzing results.

### Master-Slave D Flip-Flop Schematic Design :
  The D Flip-Flop is implemented using NMOS and PMOS transistors in a CMOS configuration.
  ![image](https://github.com/abdulkhajashabuddin16/4bit_SISO_SIPO_Shift_Register/blob/main/DFF_Schematic_Sim_AvgPower_Delay_Screenshots/DFF_Schematic.png)
  #### Master-Slave D Flip Flop Result:
  ![image](https://github.com/abdulkhajashabuddin16/4bit_SISO_SIPO_Shift_Register/blob/main/DFF_Schematic_Sim_AvgPower_Delay_Screenshots/DFF_Result.png)


### Serial-In Serial-Out (SISO)
A **SISO shift register** takes in serial input data (one bit at a time) and shifts it sequentially, outputting it in the same serial manner after a set number of clock cycles. It is primarily used for temporary data storage and data transfer applications.

#### Truth Table for 4-bit SISO Shift Register
| Clock Cycle | Q1 (MSB) | Q2 | Q3 | Q4 (LSB) |
|-------------|----------|----|----|----------|
| 0           | 0        | 0  | 0  | 0        |
| 1           | D_in     | 0  | 0  | 0        |
| 2           | D_in     | D_in | 0  | 0        |
| 3           | D_in     | D_in | D_in | 0        |
| 4           | D_in     | D_in | D_in | D_in   |

### Pre Simulation Result SISO
![image](https://github.com/abdulkhajashabuddin16/4bit_SISO_SIPO_Shift_Register/blob/main/SISO_Schematic_Sim_AvgPower_Delay_Screenshots/SISO_Trans-Analys(PRE-sim).bmp)
### Post Simulation Result SISO
![image](https://github.com/abdulkhajashabuddin16/4bit_SISO_SIPO_Shift_Register/blob/main/SISO_Schematic_Sim_AvgPower_Delay_Screenshots/SISO_Trans-Analys(POST-sim).png)
### Serial-In Parallel-Out (SIPO)
A **SIPO shift register** accepts serial input data but allows access to the data in parallel after all bits have been entered. This configuration is commonly used for serial-to-parallel data conversion.

#### Truth Table for 4-bit SIPO Shift Register
| Clock Cycle | Q1 (MSB) | Q2 | Q3 | Q4 (LSB) | Parallel Output |
|-------------|----------|----|----|----------|-----------------|
| 0           | 0        | 0  | 0  | 0        | 0000            |
| 1           | D_in     | 0  | 0  | 0        | 0001            |
| 2           | D_in     | D_in | 0  | 0        | 0011            |
| 3           | D_in     | D_in | D_in | 0        | 0111            |
| 4           | D_in     | D_in | D_in | D_in   | 1111            |

### Pre Simulation Result SIPO
![image](https://github.com/abdulkhajashabuddin16/4bit_SISO_SIPO_Shift_Register/blob/main/SIPO_Schematic_Sim_AvgPower_Delay_Screenshots/SIPO_Trans-Analys(PRE-sim).png)
### Post Simulation Result SIPO
![image](https://github.com/abdulkhajashabuddin16/4bit_SISO_SIPO_Shift_Register/blob/main/SIPO_Schematic_Sim_AvgPower_Delay_Screenshots/SIPO_Trans-Analys(POST-sim).png)
