# Analog-IC-Design-Internship-2025
Analog IC Design Course during Summer of 2025
# Analog IC Design Internship – USB Microphone AFE (Sky130)
This repository documents my internship project as a student of Silicon University, conducted in June 2025 under the mentorship of Dr. Saroj Rout. The project focuses on designing an Analog Front-End (AFE) for a USB Microphone using open-source EDA tools and the Skywater 130nm PDK. I gained hands-on experience in the complete analog IC design flow—from system-level specifications to schematic design, simulation, layout, and verification—utilizing open-source EDA tools such as Xschem, NGSpice, Magic VLSI, and Netgen, built on the Skywater 130nm CMOS PDK.
The primary focus of this project was the design and implementation of an Analog Front-End (AFE) for a USB Microphone, alongside the development and analysis of foundational analog building blocks including current mirrors, differential pairs, and folded cascode operational amplifiers. Python-based simulation and characterization scripts were also employed for design validation.
This repository serves as a structured, version-controlled archive of my design journey, technical learnings, and project deliverables in analog VLSI.

## Table of Contents
- [Project Description](#project-description)
- [Tools & Technologies](#tools--technologies)
- [Design Flow](#design-flow)
- [Results](#results)
- [Acknowledgements](#acknowledgements)

## Project Description

The objective of this project was to design and characterize analog building blocks and a complete analog front-end for a USB microphone. The key components include:

- Current Mirrors
- Differential Pair Amplifiers
- Folded Cascode Operational Amplifiers
- Complete AFE Architecture

Design, simulation, layout, and LVS/DRC were done using Sky130 CMOS process tools.

Introduction to an electronic system design-USB-MIDI microphone.
-	Microphone pre-amplifier and interface circuit design.
-	Select an widely available Op-Amp for the preamplifier e.g. TI OPA 344
-	Derive the important specs for the CMOS Op-Amp design.
- Derive also all the specs for the circuit Design and analysis.

Introduction to linear circuits and passive devices.
-	Understanding passive devices (RLC) using basic EM principles.
-	Principle of linearity and superposition
-	Network analysis: KCL, KVL, Thevenin, Norton, Superposition.
-	Emphasis on interfacing circuits and power transfer principle.

Introduction to all the Fundamentals
- Understanding the BJT fundamentals.
-	Understanding of MOS Transistor.
- Understanding the Semiconductor IC Devices.
________________________________________
RESOURCES & REFRENCES
1.	PDK & DRC Manual PDK.
2.	MEMS mic Datasheet.
3.	OP-AMP-344 Datasheet.
4.	Schematic Sparkfun breakout Board.

## Tools & Technologies

- Skywater 130nm PDK
- Xschem – Schematic Entry
- NGSpice – Circuit Simulation
- Magic VLSI – Layout Editor
- Netgen – LVS Verification
- Python – Automation and Plotting

## Design Flow

1. Define system-level specifications for the USB Mic AFE.
2. Design individual blocks in Xschem.
3. Simulate using NGSpice.
4. Layout design using Magic VLSI.
5. Perform DRC & LVS verification using Magic and Netgen.
6. Run Python-based analysis on simulation results.

## Results
### Schematic:
[HighPassFilter](images/HighPassFilter.png)
## Buffer Op-Amp Stage

Used to isolate load and maintain signal integrity. The buffer has a unity gain and is placed after the filter stage.

### Schematic:
[BufferStage](images/oio.png)
## Simulation Results

Simulations are done in **Ngspice** using `.ac` and `.tran` analysis to verify:

- Gain Amplification
- Behaviour of the filter (cutoff around 6.77 Hz)
-  Flow of Signal across buffer

### Example Output:

[Simulation Waveforms](images/plot01.png)

###  Thevenin's Model of a Microphone
<ul>
    The Circuit demonstrates a practical application of Analog Design Principle
     <img width="1366" height="768" alt="Screenshot (452)" src="https://github.com/user-attachments/assets/1f70b55f-26a8-4c96-82fc-65cfc9732d2f" />

</ul>
###  NMOS Operational Amplifier
<ul>
    In an n-channel E-MOSFET, a positive gate voltage creates a conducting path by attracting electrons.                                                                                        
    <img width="1366" height="768" alt="Screenshot (550)" src="https://github.com/user-attachments/assets/5066ffb6-2c2d-4c2e-a6b0-5a3a946f4816" />

</ul>

###  Differential Amplifier
<ul>
    It amplifies the difference between two input signals and is widely used in analog signal processing, especially in operational amplifiers.                                            
    <img width="1366" height="768" alt="Screenshot (551)" src="https://github.com/user-attachments/assets/6d8f973a-37df-4bee-8dab-4b0529a8e832" />

</ul>

###  Siliwiz Simulation 
<ul>
     SiliWiz uses a SPICE simulator to turn what you've drawn into a functional circuit.                                                                                            <img width="1366" height="768" alt="Screenshot (535)" src="https://github.com/user-attachments/assets/d1dbcf04-e3bc-4a6c-89d6-d4776bdb383f" />

</ul>

###  High-Pass Operational Amplifier
<ul>
    A high pass filter will allow the frequencies which are higher than the cut-off frequency and attenuate the frequencies lower than the cut off frequency.                        <img width="1366" height="768" alt="Screenshot (506)" src="https://github.com/user-attachments/assets/d1bcf30c-57ce-48ce-8559-e2aa42707908" />

</ul>     

###  Current Mirror
<ul>
    The circuit is used to copy the flow of current in one active device and controlling the flow of current in another device by maintaining the output current stable instead of loading
    <img width="1366" height="768" alt="Screenshot (659)" src="https://github.com/user-attachments/assets/59672732-fc8f-461c-994e-70189e13d307" />

</ul>

###  Operational Amplifier
<ul>
    An Operational Amplifier, or Op-amp for short, is fundamentally a voltage amplifying device designed to be used with external feedback components such as resistors and capacitors between its output and input terminals.
    <img width="1366" height="768" alt="Screenshot (660)" src="https://github.com/user-attachments/assets/7f2f72be-6ccd-4aa3-866b-07c075de1a5b" />

</ul>

###  Small Signal Analysis
<ul>
    Devices like BJTs or MOSFETs have non-linearly but when the input signal is small, we can approximate the device as linear around its operating point.
    This approximation is known as Small Signal Analysis.
    <img width="1366" height="768" alt="Screenshot (546)" src="https://github.com/user-attachments/assets/ed4bba97-cef7-4120-92f8-d45b17e58b7f" />

</ul>



## Acknowledgements

I would like to thank Dr. Saroj Rout for his mentorship and guidance throughout the internship. Gratitude also to Silicon University and the open-source EDA community for enabling this work.




