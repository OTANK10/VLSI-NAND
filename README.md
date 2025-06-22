# VLSI NAND Gate Design and Analysis

This project demonstrates the complete VLSI design flow from schematic capture to physical layout verification and performance characterization. The design implements a 2-input NAND gate optimized for a standard cell library with detailed timing and power analysis.

![image](https://github.com/user-attachments/assets/916280ba-2055-4dd1-b464-c63aa3aeb8f9)  

* Key Achievements
 
✅ Functional NAND gate design meeting all specifications  
✅ DRC and LVS clean layout in 45nm technology  
✅ Comprehensive timing characterization (tpdr: 35.1ps, tpdf: 38.3ps)  
✅ Power analysis including leakage (21.8nA) and peak current (243µA)  
✅ Supply voltage sensitivity analysis (0.85V - 1.10V)  
✅ Parasitic extraction and post-layout verification  

* Tools and Technologies

Design Tools: Cadence Virtuoso (Schematic XL, Layout GXL)  
Verification: Cadence Pegasus (DRC, LVS, PEX)  
Simulation: Synopsys HSPICE, Cscope  
Technology: GPDK 45nm CMOS process  
Design Kit: gpdk045  

* Design Specifications

Transistor Sizing  

Technology: 45nm minimum channel length  
β ratio: 2 (PMOS/NMOS width ratio)  
Minimum width: 120nm (NMOS), 240nm (PMOS)  
Series optimization: Properly upsized for stacked transistors  

* Layout Constraints  

Cell height: 3µm standard cell compatible  
Power rails: 300nm M1 rails (VDD top, GND bottom)  
Metal layers: M1 horizontal, M2 vertical routing only  
I/O placement: Inputs left (M1), outputs right (M1)  

* Performance Targets  

Supply voltage: 1.1V nominal  
Load: 8 minimum inverters + 6fF wire capacitance  
Input timing: 30ps rise/fall times (20%-80%)  

# Results Summary

![image](https://github.com/user-attachments/assets/5c90b593-f0fb-4b74-8b68-4137882cb941)


* Analysis Methodology
  
1. Functional Verification  

Complete truth table verification using digital vector simulation  
HSPICE transient analysis with proper load modeling  
Input/output timing relationship validation  

2. Timing Analysis  

Propagation delay measurement (50%-50% metric)  
Rise/fall time characterization (20%-80% metric)  
Load capacitance impact assessment  
Parasitic extraction effects quantification  

3. Power Analysis  

Static leakage current measurement during steady-state  
Dynamic peak current during switching transitions  
Supply current source methodology with 0V meters  
Exclusion of load inverter channel currents  

4. Process Sensitivity  

Supply voltage sweep analysis (0.85V - 1.10V)  
Delay vs. VDD characterization  
Leakage vs. VDD relationship  
Input signal integrity verification  


