# FPGA Oscilloscope

## Table of Contents
- [Intorduction](#intorduction)
- [Directory Tree](#directory-tree)
- [Project Info](#project-info)
- [Framework and Layout](#framework-and-layout)
- [Contributor](#contributor)

## Intorduction
We built a simple oscilloscope using Nexys 4 DDR board and PCB. First, the PCB transforms the input voltage signal into a signal with an acceptable voltage range for the FPGA board input, as well as generating knobs' control signal. The FPGA board then takes the processed signal and control signal to display waveforms, change voltage scale, adjust sweep time, etc. This work is the final project of the Digital Laboratory class at NCTU. [ [Demo Video](https://www.youtube.com/watch?v=sgIzcKYEROs&feature=youtu.be&ab_channel=AlexLi) ]

## Directory Tree
<pre>
FPGA_Oscilloscope/
├─ Demo Video/ ..................... 
│  └─ Demo Video.mp4 ............... 
├─ FPGA_Code/ ...................... System Verilog code for oscilloscope
│  ├─ Oscilloscope.sv .............. Main Function
│  ├─ Control.sv ................... Function for processing control signal
│  ├─ Sampling.sv .................. Function for sampling signal
│  ├─ Data_transfer.sv ............. Choose sample data based on scale
│  ├─ Sampling_time.sv ............. Choose sample time based on scale
│  ├─ VGA.sv ....................... Function for displaying information on screen.
│  ├─ Trig_display.sv .............. Display trigger info
│  ├─ Time_display.sv .............. Display time info
│  ├─ Channel_display.sv ........... Display waveform
│  ├─ Info_display.sv .............. Subfunction for displaying info
│  ├─ Trig_info.sv ................. Subfunction for displaying info
│  ├─ Time_info.sv ................. Subfunction for displaying info
│  ├─ Scale_tag.sv ................. For output scale
│  ├─ Word.sv ...................... For bitmap-fonts
│  ├─ Word_move.sv ................. For bitmap-fonts
│  ├─ DFF.sv ....................... D Flip flop
│  ├─ clk_div_2.sv ................. Clock
│  ├─ Clk_div_4.sv ................. Clock
│  ├─ clk_div_16.sv ................ Clock
│  └─ clk_div_256.sv ............... Clock
└─ PCB/ ............................ Input rectifier circuit design
   ├─ MAX6818.lbr .................. ICL7660CAS Library File
   ├─ Oscilloscope.brd ............. PCB board file
   ├─ Oscilloscope.sch ............. PCB schematic file
   └─ Gerber/ ...................... Directory contains layout files
</pre>

## Project Info
- **HDL**: [SystemVerilog](https://en.wikipedia.org/wiki/SystemVerilog)
- **FPGA Board**: [Nexys 4 DDR](https://reference.digilentinc.com/reference/programmable-logic/nexys-4-ddr/start)
- **PCB Layout Software**: [EAGLE](https://www.autodesk.com/products/eagle/overview?plc=F360&term=1-YEAR&support=ADVANCED&quantity=1)

## Framework and Layout
![project picture](https://github.com/Hong-Ming/FPGA_Oscilloscope/blob/main/Images/project.png)
**Framework**:
![framework](https://github.com/Hong-Ming/FPGA_Oscilloscope/blob/main/Images/framework.png)
**Input Rectifier Circuit Schematic**:
![input circuit schematic](https://github.com/Hong-Ming/FPGA_Oscilloscope/blob/main/Images/input_schematic.png)
**Input Rectifier Circuit Layout**:
![input circuit layout](https://github.com/Hong-Ming/FPGA_Oscilloscope/blob/main/Images/input_layout.png)

## Contributor
- [Hong-Ming Chiu](https://hong-ming.github.io/)
- [Huan-Jung Lee]()
