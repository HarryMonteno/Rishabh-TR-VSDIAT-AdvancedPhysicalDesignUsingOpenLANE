![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/02760a0f-17c0-4ca6-a8d4-9768f92ce696)![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/2346e6fc-2176-4a13-b7d4-11b8b4b6a37c)![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/22ae1bfe-5e79-47e4-bf16-879c73d2c957)![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/bcbf0578-a172-42ab-9ecc-aed989e1d87b)![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/a420e848-6fc6-4758-b273-ce0cccfe2349)# Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE
This repository documents my progress in the VSDIAT Advanced Physical Design course, where I utilized the SkyWater 130nm PDK and open-source EDA tools.

Day 1
Introduction
Day_1 Introduction to Open-Source EDA, OpenLANE & Sky130PDK

![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/9882fc9e-c7c8-47f4-91c1-72c67e40afa4)

# SKY130 Day 1: Introduction to OpenSource EDA, OpenLANE, and SKY130 PDK
![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/378dc88a-9c4d-4991-9ac2-35dba7ab2af5)

## Communicating with Computers

### Understanding QFN - 48 Package and Its Components

The Arduino circuit board, a widely used microcontroller platform, features a System on a Chip (SoC) at its core, surrounded by a Quad Flat No-Leads (QFN) - 48 package. This package encapsulates the chip, and its schematic representation resembles a block diagram, showcasing various components such as PADS, CORE, and DIE.

### Exploring RISC V Architecture

The RISC-V Instruction Set Architecture (ISA) serves as the language for computers. Compiling a C program for hardware involves converting it into an assembly language like RISC V, then into machine language, and eventually implementing it in hardware.

### Bridging Software Applications to Hardware
![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/83084ff3-338f-411b-9433-a515966043bb)

Software applications, or apps, run on hardware like laptops, mobile phones, and tablets, powered by chips. These apps are coded in complex programs that require conversion into binary or machine language. This conversion is facilitated by system software, including operating systems, compilers, and assemblers.

## SoC Design and OpenLANE

### Components of Opensource Digital ASIC Design

Application-Specific Integrated Circuit (ASIC) design requires RTL IPs, EDA Tools, and PDK data. Until recently, there was no open-source PDK data available, but Google and Skywater's release of PDK data for 130 nm chips changed this, making ASIC design possible on open-source platforms.

### The Simplified RTL to GDS Flow

The RTL to GDSII (Graphic Design System II) design process involves several steps, including synthesis, floor planning, placement, clock tree synthesis, routing, sign-off, and various verification processes like DRC, LVS, and STA.

### Introduction to OpenLANE and Strive Chipsets

OpenLANE is an open-source digital ASIC automation tool, developed by efabless and Google, aiming to automate the entire design process flow. Strive chipsets are SoCs created by Efabless, part of the OpenLANE ecosystem.

### OpenLANE Detailed ASIC Design Flow

The detailed ASIC design flow using OpenLANE includes synthesis exploration, design exploration, regression testing, design for test, physical verification, logic equivalence check, and addressing antenna rules violations, among other steps.

## Getting Familiar with Opensource EDA Tools

### Exploring OpenLANE Directory Structure

OpenLANE is a flow comprising various open-source EDA tools. Exploring the OpenLANE directory structure involves navigating through directories like pdks and openlane, which contain essential files and configurations for ASIC design.

### Design Preparation Step

Setting up a design in OpenLANE involves preparing the design, ensuring that the final product functions correctly. This step involves setting up a filesystem, creating folders, and generating necessary files for the design.

### Reviewing Files After Design Prep and Running Synthesis

![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/e2e71354-57d0-466b-82f7-8e6e8fc54045)
![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/81d5ea45-4e6e-488d-b8f3-0112794ed955)
![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/d55fe62b-4ab5-42f7-b0e5-7d38b137898b)

After preparing the design, running synthesis converts the abstract netlist into a program. This step involves running yosys RTL synthesis, ABC scripts for technology mapping, and openSTA, providing valuable statistics and reports for analysis.

### Characterizing Synthesis Results

Analyzing the synthesis results involves calculating the flip-flop ratio and reviewing the synthesis output files to ensure the design meets the required specifications. This step provides insights into the design's performance and functionality.

### Exploring Clock Timing Report

After running synthesis, it's important to review the clock timing report to ensure that the design meets the required timing constraints. This report provides details about the timing paths in the design, including setup and hold times, clock delays, and critical paths.

## Summary

In summary, Day 1 of the SKY130 workshop introduced key concepts in open-source EDA tools, focusing on OpenLANE and the SKY130 PDK. Participants learned about the components of digital ASIC design, the RTL to GDSII flow, and the detailed ASIC design flow using OpenLANE. They also gained familiarity with the OpenLANE directory structure, design preparation steps, and synthesis result characterization.

Overall, the workshop provided a comprehensive overview of open-source EDA tools and their applications in digital ASIC design, setting the stage for further exploration and hands-on experience in subsequent sessions.

# SKY130 Day 2: Exploring Floorplans and Introduction to Library Cells
## Understanding Chip Floor Planning Concepts
### Utilisation Factor and Aspect Ratio
The initial step in physical design involves defining the width and height of the core and die. Starting with a basic netlist, we create a symbolic diagram, which will later be transformed into physical designs. Each cell, whether a gate or a specific cell like a flip-flop, is given standard dimensions. For example, each unit is 1x1 unit in size, so with 4 gates/flip-flops, the total size of the silicon wafer is 4 sq. units.

All logical cells are placed inside the core, which is part of the die. The utilization factor is the ratio of the area occupied by the netlist to the total core area. Although the utilization factor may theoretically reach 100%, it typically remains around 50%. The aspect ratio is the ratio between height and width, where a square chip has an aspect ratio of 1, while a rectangular chip has a different ratio.
![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/6714f7ab-a4ff-43d7-965f-666b573ae4df)
![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/d864a600-8515-41b0-9fb8-1deaf749b351)
![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/4a328f34-fc1a-4871-a0cd-37e48b9a8977)
![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/fe1daba4-c571-4591-a5be-f9bed41af305)



### Understanding Pre-Placed Cells

Pre-placed cells are complex logic blocks that are reusable and already implemented, which cannot be modified by Auto Place and Route tools. Their placement is user-defined. By dividing the logic into blocks while maintaining connectivity, we can create blackboxed sections that can be used as needed. These pre-placed blocks can include memory, clock-gating cells, comparators, and MUXes. The arrangement of these blocks on a chip is known as floorplanning.

### Addressing Decoupling Capacitors

To stabilize pre-placed cells, we surround them with decoupling capacitors. When a circuit is switched on, there is a demand for current, which is supplied by Vdd. However, due to resistance, inductance, and capacitance in the wire, the voltage supplied, Vdd', can be slightly reduced, potentially causing instability. Decoupling capacitors act as a buffer, ensuring stable power supply to the cells.

### Strategies for Power Planning

When dealing with a macro that requires a large voltage, such as a 16-bit bus connected to an inverter, it's important to consider the discharge of capacitors, which can lead to Ground Bounce, and the possibility of Voltage Drop due to insufficient current. To address these issues, a power mesh with multiple power source taps and sinks can be used, allowing capacitors to source current from the nearest Vdd and sink current to the nearest Ground.

### Pin Placement and Logical Cell Placement Blockage

In chip design, the placement of input and output ports, clock ports, and logical cells is crucial. Clock ports are larger than data ports, and the size is inversely proportional to resistance. Logical cell placement blockage ensures that the APR tool does not place any cell on the pin locations, ensuring proper connectivity.

### Running Floorplan Using OpenLANE

Before running the floorplan, configuration variables or switches must be set, which are located in the openlane/configuration directory. The configuration settings are stored in openlane/designs/[design-date]/config.tcl. The vertical and horizontal metal specifications in OpenLANE are set one higher than what is specified. The floorplan can be executed in OpenLANE using the command run_floorplan.

### Reviewing Floorplan Files and Layout
![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/761bebe5-e3cf-43be-84db-23b95316dc46)
![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/4eebb910-289c-4240-bf29-4aa5281e4307)
![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/dd93a955-3c65-4924-8ffc-b8b52d8c6f40)

After running the floorplan, the results are stored in a design exchange format, containing the die area and positions. The die area is in database units, where 1 micron equals 1000 database units. The floorplan layout can be reviewed using Magic, a layout tool, to inspect the layout and ensure proper placement of components.

## Library Binding and Placement
### Netlist Binding and Initial Placement Design

The process of binding the netlist with physical cells involves selecting cells from the standard cell library that meet the design requirements. The placement of these cells is based on connectivity, ensuring that related cells are placed close to each other to reduce delay.

### Optimizing Placement Using Estimated Wire-Length and Capacitance

Estimating the wirelength needed to connect components together is essential for determining if repeaters are necessary. Repeaters are used to recondition signals that may change over long distances. Final placement optimization aims to minimize wirelength and optimize placement for better performance.

### Congestion-Aware Placement Using RePLACE

The placement in OpenLANE is performed using the RePlace tool, which focuses on global placement without legalisation, using the HPWL reduction model. The placement aims to converge the overflow value progressively, ensuring that designs are stable and meet the required specifications.

## Cell Design and Characterisation Flows
### Inputs for Cell Design Flow and Circuit and Layout Design Step

The standard cell library contains various cells with different functionalities and variations in drive strengths, functionality, and voltages. The standard cell design flow involves circuit and layout design to meet the input library requirements. The design flow adheres to DRC and LVS rules, SPICE models, and user-defined specifications to ensure compatibility and functionality.

### Typical Characterisation Flow

Characterisation involves reading SPICE model files, netlists, recognizing buffer behavior, attaching power sources, applying stimulus, providing necessary output capacitance, and simulating the circuit to generate timing, noise, and power models in the form of .libs files.

## General Timing Characterisation Parameters
### Timing Threshold Definitions
![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/75ba40e8-d8c6-4b34-ae7a-7b1c318c5e59)
![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/4eaa2114-1eef-4c79-a775-49107a7e2a4e)

Understanding timing thresholds is crucial for ensuring proper circuit behavior. Propagation delay is calculated as the time taken for an output to respond to a change in the input, while transition time is the time taken for a signal to change from one logic level to another. Proper threshold values must be selected to avoid unexpected results and ensure stable operation of the circuit.

Sure, let's continue from where we left off:

### General Timing Characterization Parameters
#### Timing Threshold Definitions

Understanding timing thresholds is crucial for ensuring proper circuit behavior. Propagation delay is calculated as the time taken for an output to respond to a change in the input, while transition time is the time taken for a signal to change from one logic level to another. Proper threshold values must be selected to avoid unexpected results and ensure stable operation of the circuit.

#### Understanding Setup and Hold Time

Setup time is the minimum amount of time before the clock's active edge that the data must be stable for the flip-flop to capture it correctly. Hold time is the minimum amount of time after the clock's active edge that the data must remain stable. Violating setup and hold times can lead to metastability, where the flip-flop fails to settle in a stable state, causing unpredictable behavior.

#### Clock-to-Q Delay and Maximum Operating Frequency

Clock-to-Q delay is the time taken for the output of a flip-flop to respond to a clock edge. It is crucial for determining the maximum operating frequency of a circuit. By minimizing clock-to-Q delay, the maximum operating frequency can be increased, improving the performance of the circuit.

#### Timing Margins and Critical Path Analysis

Timing margins are the difference between the actual timing values and the minimum required timing values. Positive margins indicate a robust design, while negative margins indicate potential timing violations. Critical path analysis involves identifying the longest path in the circuit and ensuring that it meets timing requirements to avoid timing violations.

#### Importance of Timing Analysis in Floorplanning

Timing analysis is essential in floorplanning to ensure that the placement of cells and routing of signals meet timing requirements. By analyzing timing at the floorplanning stage, designers can identify and address potential timing violations early in the design process, minimizing the need for costly redesigns later on.

#### Conclusion

In conclusion, understanding the various aspects of chip floor planning, library cells, and timing characterization is crucial for designing robust and high-performance integrated circuits. By following best practices and utilizing tools like OpenLANE, designers can optimize their designs for performance, power, and area, meeting the stringent requirements of modern semiconductor devices.

# SKY130 DAY 3: Design Library Cell Using Magic Layout and NGSPICE Characterization
## Labs for CMOS Inverter NGSPICE Simulations
### IO Placer Revision
![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/6f1ea3e6-1da3-4716-a5eb-c755a22b292c)

![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/eda6e921-9784-408e-ad99-5a8b89cb4ceb)

![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/00ff30bf-de73-4f9a-b5bc-3520cf9270ec)

![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/dcbb9e0e-805f-48da-b52d-7bc8f8fec197)

![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/e286c847-ec5f-4263-b6a8-468f241e47fb)


Configuration changes in OpenLANE can be made on the fly within the shell itself. The IO Mode is typically set to "random equidistant." To change this, use the following command after the floorplan step: **set ::env(FP_IO_MODE) 2**. This command will change the IO (input-output) pins to mode 2, where they are no longer equidistant (as in the default mode, which is 1).

After running this command, re-run the floorplan step. You will notice that the pins are now placed using Hungarian algorithms, stacked one over the other.

> Note: Changing the configuration on the fly will not update the `runs/config.tcl` file. The configuration changes will be effective only for the current session.

### SPICE Deck Creation For CMOS Inverter

The SPICE deck contains connectivity information about netlists, inputs, and TAPS for the outputs. The component values are typically set to .375u/.25u for PMOS (channel length of .25 micron and channel width of .375 micron). The PMOS should ideally be 2 to 3 times wider than the NMOS to match rise and fall times, as the PMOS carrier is slower than the NMOS carrier.

Node identification and naming are crucial in SPICE deck netlists. The syntax for PMOS and NMOS is: _[component name] [drain] [gate] [source] [substrate] [transistor type] W=[width] L=[length]_. All components in a netlist are described based on their nodes and values.

### SPICE Simulation Lab for CMOS Inverter

SPICE simulation begins with _.op_, where Vin is swept from 0 to 2.5 with 0.05V steps. The model file **tsmc_025um_model.mod** contains technological parameters for the 0.25µm NMOS and PMOS.

For SPICE simulation, follow these steps:

1. Open the NGSPICE simulator.
2. Source the Circuit File using the _source_ command.
3. Execute the command _run_, and then use _setplot_ to view any plots possible from the simulations specified in the spice deck, providing a choice for which simulation to run.
4. Type _display_ to choose nodes to be plotted. Typing _plot out vs in_ will plot them on a graph.

### Switching Threshold Vm
![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/5004d006-3fbb-40ba-9a1c-8dc9f6490ce9)

The switching threshold is the point where the input voltage equals the output voltage, and both PMOS & NMOS are in the saturation region. This state can lead to leakage and potential short circuits.

### Static and Dynamic Simulation of CMOS Inverter
![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/7a560260-40b4-4249-aa4f-5575c7e88221)

To find Vm, use DC TRANSFER ANALYSIS. Simulation is a sweep from 0V to 2.5V by 0.05V steps.

To find propagation delay, use transient analysis when a pulse is applied to the CMOS.

### Lab Steps to GitClone VSDSTD Cell Design

Clone the custom inverter standard cell design from the provided GitHub repository. Steps include cloning the repository, copying the tech file to the created directory, and opening the custom inverter layout in MAGIC.

## Inception of Layout and CMOS Fabrication Process

The 16 MASK CMOS Fabrication process involves several steps:

1. Create Active Regions: Select a substrate, grow Silicon Dioxide, deposit Silicon Nitride, deposit a layer of photoresist, deposit mask-1 layer, apply UV light, remove mask-1 and photoresist layers, place the chip in the furnace to grow oxide in other areas, and remove the Si3N4 layer using hot phosphoric acid.

2. Formation of N and P Well: Use Mask 2 and 3 to protect N-Well and P-Well areas while boron and phosphorous are diffused to form wells.

3. Formation of Gate Terminal: Use photolithography to define gate areas, implant low-energy boron for p-well, and implant phosphorous/arsenic for n-well. Create spacers using plasma anisotropic etching and add polysilicon film for the gate.

4. Lightly Doped Drain (LDD) Formation: Use Mask 7 and 8 for NMOS and PMOS, respectively, to create lightly doped regions to prevent hot electron effect and short channel effect.

5. Source and Drain Formation: Create contact holes, deposit thin screen oxide, and implant N+/P+ impurities for actual source and drain.

6. Local Interconnect Formation: Remove screen oxide to open up source, drain, and gate for contact building. Use Titanium for less resistance and Titanium Diselenide for local interconnects.

7. Higher Level Metal Formation: Deposit Silicon Dioxide doped with phosphorous or boron, polish the surface using CMP, create contact holes through photolithography, and use various masks for different contact layers.

## SKY130 Tech File Labs
### Lab Steps To Create Final SPICE Deck using SKY130 Tech

Modify the default SPICE deck file using Sky130 to plot a transient response by editing it to include transient analysis. Load the SPICE file for simulation in NGSPICE using the![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/369559c5-fdac-4e0b-ad63-805f0cafa9f4)
 command _ngspice sky130A_inv.spice_.
![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/47a2bf89-0d3e-4fa7-9fd8-bd587eeea96c)
![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/87077171-b18e-417e-b21a-82963bab2bb2)
![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/0e3abd0a-4e72-4aae-b7e3-f8efa0b1888a)
![Uploading image.png…]()

### Lab Steps to Characterize Inverter using SKY130 Model Files

Generate a graph to characterize the cell by analyzing four parameters: rise transition, fall transition, fall cell delay, and rise cell delay. These parameters help understand the behavior of the inverter.

### Lab Introduction to Magic Tool Options and DRC Rules

Learn how MAGIC performs DRC (Design Rule Check) and understand the syntax for the rules.

### Lab Introduction to SKY130 PDKs And Steps to Download Labs

Download the lab files using the command _wget http://opencircuitdesign.com/open_pdks/archive/drc_tests.tgz_ and extract them using _tar xfz drc_tests.tgz_.

### Lab Introduction to Magic and Steps to Load SKY130 Tech Rules

Open MAGIC and load the SKY130 tech rules to analyze layouts for DRC errors and fix them as necessary.

### Lab Exercise to Fix poly.9 Error in SKY130 Tech-File

Modify the SKY130 tech file to include rules for poly-resistor spacing to diffusion and tap, ensuring adherence to DRC rules.

### Lab Exercise to Implement Poly-Resistor Spacing to Diff and Tap

Adjust the tech file to include rules for poly-resistor spacing to all types of diffusion, correcting the spacing errors.

Sure! Continuing from where we left off:

To fix the error shown in the previous screenshot, we need to add rules for the spacing between npolyres and all types of diffusion in the sky130A.tech file. Below is the modification made to include these rules:

```tcl
  # Poly spacing to active
  poly.9 all {NPDIFF} 0.48
  poly.9 all {PPDIFF} 0.48
  poly.9 all {DIFF} 0.48
```

After saving these changes, we can re-run the DRC check in the Magic tool to verify that the error has been fixed.

### Lab Exercise to Implement Poly-to-Poly and Tap Spacing

In this exercise, we need to fix the spacing between poly-to-poly and tap. The error indicates that the spacing should be at least 0.45um. To fix this, we need to add a new rule in the sky130A.tech file:

```tcl
  # Poly to poly and tap spacing
  poly.9 all poly:poly_tap 0.45
```

After saving the changes and re-running the DRC check, the error should be resolved.

### Lab Exercise to Implement M1-M2 Contact Spacing

The error indicates that the spacing between M1-M2 contacts should be at least 0.1um. To fix this, we need to add a new rule in the sky130A.tech file:

```tcl
  # M1-M2 contact spacing
  contact 1 1.5 0.1
```

After saving the changes and re-running the DRC check, the error should be resolved.

### Lab Introduction to Sky130 PDK DRCs and Steps to Load Techfile

To load the techfile in the Magic tool, we can use the following command:

```sh
magic -T sky130A.tech
```

After loading the techfile, we can perform various layout operations using the SkyWater PDK rules.

### Lab Steps to Load a Layout in Magic Tool

To load a layout in the Magic tool, we can use the following command:

```sh
magic -T sky130A.tech layout_name.mag
```

This will load the specified layout file using the SkyWater PDK rules.

### Lab Exercise to Simulate M1-M2 Contact Spacing

In this exercise, we need to simulate the spacing between M1-M2 contacts to ensure that it meets the DRC requirements. We can do this by loading the layout in the Magic tool and performing the DRC check. If there are any spacing violations, we need to fix them in the layout.

### Lab Introduction to Euler's Path

Euler's path is a concept used in graph theory to determine if a graph has a path that visits each edge exactly once. It is named after the Swiss mathematician Leonhard Euler, who first studied it in the 18th century. In the context of physical design, Euler's path can be used to optimize routing paths to minimize wirelength and improve overall layout efficiency.

### Lab Introduction to SPICE Decks and Extraction

SPICE decks are files that contain information about the circuit to be simulated, including component values, connectivity, and simulation parameters. SPICE extraction is the process of extracting parasitic information from a layout to include in the SPICE deck for more accurate simulations.

### Lab Steps to Create a SPICE Deck and Extract Parasitics

To create a SPICE deck and extract parasitics, we can use the following steps:

1. Load the layout in the Magic tool.
2. Run the extraction tool to extract parasitics.
3. Create a SPICE deck that includes the extracted parasitics.
4. Simulate the circuit using the SPICE deck to verify its behavior.

By following these steps, we can create an accurate SPICE model of the layout for simulation.

### Lab Exercise to Simulate a Layout Using SPICE

In this exercise, we need to simulate a layout using SPICE to verify its functionality. We can do this by creating a SPICE deck that includes the extracted parasitics and simulating the circuit using a SPICE simulator. The simulation results can then be analyzed to ensure that the layout meets the design requirements.

### Lab Conclusion

In conclusion, the labs in this course cover a wide range of topics related to physical design using the SkyWater 130nm PDK. From layout design to simulation and verification, these labs provide a comprehensive overview of the physical design process and the tools used in the industry. By completing these labs, students can gain valuable hands-on experience in physical design and prepare themselves for a career in the semiconductor industry.

# SKY130 DAY 4: Pre-Layout Timing Analysis and the Importance of a Good Clock Tree
## Timing Modeling Using Delay Tables
### Converting Grid Information into Track Information

The file `sky130_inv.mag` located in the `vsdstdcelldesign` directory contains information like power and ground rails, and input/output information. OpenLANE, being a PnR tool, does not require the full information present in the `.mag` file. We only need the boundary, power and ground rails, and the inputs & outputs information, which is why we use `.lef` files. Our next objective is to extract the LEF file from the MAGIC file and plug that into the picorv32a design. The guidelines to be followed while making a standard cell are:

1. The input and output ports must lie at the intersection of the horizontal and vertical tracks (this ensures the routes can reach the ports).
2. The width and height of the standard cell must be odd multiples of the track's horizontal and vertical pitch, respectively.

> Tracks refer to the horizontal and vertical metal layers on which routing occurs. The grid formed by the intersection of horizontal and vertical tracks creates a routing grid, also known as a routing matrix.

The `tracks.info` file contains track information. Before and after changing the grid values:


Hence, we are able to satisfy the first guideline.


Then, we are able to satisfy the second guideline as follows:


### Converting Magic Layout to STD Cell LEF

LEF (Library Exchange Format) files contain information about the standard cell library used in the design, detailing geometric shapes, sizes, layers, and other physical properties of individual cells or macros within the library. The instructions to set the port definitions are available [here](https://github.com/nickson-jose/vsdstdcelldesign#create-port-definition). Next, save the `.mag` file with a new filename by typing `lef write` in the tkcon terminal, which will generate a new `.lef` file with the new filename:



### Introduction of Timing Libraries and Steps To Include a New Cell in Synthesis

Inside the directory `pdks/sky130A/libs.ref/sky130_fd_sc_hd/lib/` are the liberty timing files for the SKY130 PDK, containing timing and power parameters for each cell needed in STA. These libraries describe different PVT corners (slow, typical, fast) with different supply voltages (1v80, 1v65, 1v95). The library named `sky130_fd_sc_hd__ss_025C_1v80` describes the PVT corner as slow-slow, 25°C temperature, at 1.8V power supply. Timing and power parameters of a cell are obtained by simulating the cell in a variety of operating conditions (different corners), represented in the liberty file. This data characterizes all cells and is used during ABC mapping during the synthesis stage to map the generic cells to the actual standard cells available in the liberty file.

- Copy the extracted LEF file (named `sky130_vsdinv.lef`) and the liberty files (named `sky130*.lib`) from this repository (`openlane/vsdstdcelldesign/libs`) to the `src` directory of `picorv32a`:

[Image 5]

- Add the following to the `config.tcl` file inside the `picorv32a` directory to set the liberty file for ABC mapping of synthesis (`LIB_SYNTH`) and for STA (`FASTEST`, `SLOWEST`, `TYPICAL`), and also the extra LEF files (`EXTRA_LEFS`) for the customized inverter cell:

[Image 6]

- Invoke the `docker` command and prepare the `picorv32a` design. Plug the new `lef` file into the OpenLANE flow through the following commands:

```
docker

./flow.tcl -interactive

package require openlane 0.9

prep -design picorv32a

set lefs [glob $::env(DESIGN_DIR)/src/*.lef]

add_lefs -src $lefs
```

This will generate the following picture:

[Image 7]

- Then, run synthesis using the `run_synthesis` command and check that the `sky130_vsdinv` cell is successfully included in the design:

[Image 8]

### Delay Tables

[Image Credits: VSDIAT; Screenshot taken from lecture]

[Image 9]

The above image shows how the enable pin affects the CLK propagation. In the case of an AND gate, CLK propagates to Y only when the enable pin is equal to 1. Similarly, in the case of an OR gate, CLK propagates to Y only when the enable pin is 0. Clock Gating Technique is used to reduce switching power consumption when such elements are used in the CLOCK TREE.

### Lab Steps To Configure Synthesis Settings to Fix Slack and Include VSDINV

After the previous steps, we observe that the timing is still above 1

 ns due to the area occupied by the inverter cell. To fix this, modify the synthesis settings as follows:

- Go to `./src` and run the synthesis again using the following commands:

```
cd ./src

run_synthesis

```

- Analyze the reports, specifically `post_synth_vsdinv.v.rpt` which shows that the slack is still not met:

[Image 10]

- To fix the slack, modify the synthesis settings inside the `config.tcl` file by adding the following lines:

```
set ::env(SYNTH_MAX_FANOUT) 4

set ::env(SYNTH_MAX_INPUT_LOAD) 4.0
```

- Run synthesis again and check the reports. The slack should now be met, as shown below:

[Image 11]

### Key Takeaways

- Tracks play a crucial role in standard cell design, ensuring that inputs and outputs are correctly placed for efficient routing.
- LEF files contain essential information about standard cells, allowing tools like OpenLANE to understand their physical characteristics.
- Timing libraries (liberty files) contain timing and power parameters for cells under different operating conditions, essential for proper synthesis and timing analysis.
- Delay tables help visualize how clock signals propagate through logic gates, crucial for understanding and optimizing timing behavior.
- Proper synthesis settings, such as maximum fanout and input load, are crucial for meeting timing constraints and optimizing design slack.

- Certainly! Continuing from where we left off:

### Clock Tree Synthesis

Clock Tree Synthesis (CTS) is a crucial step in the physical design flow of an ASIC, especially for high-performance designs. Its primary goal is to distribute the clock signal from the clock source (often a PLL or a crystal oscillator) to all sequential elements (flip-flops) in the design with minimum skew and maximum performance. A well-balanced and optimized clock tree is essential for meeting timing requirements and ensuring reliable operation of the chip.

#### Importance of a Good Clock Tree

![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/0e2fa284-fa2e-4e7a-86c2-23679d36615e)
![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/1be062c5-b205-4028-8017-e1faf9915546)

- **Clock Distribution**: The clock signal needs to be distributed evenly and with minimum skew to all sequential elements. A well-designed clock tree ensures that all flip-flops receive the clock signal at the same time, reducing setup and hold time violations.

- **Clock Jitter**: Clock jitter, caused by noise and variations in the clock signal, can lead to timing violations and affect overall chip performance. A good clock tree minimizes jitter by maintaining signal integrity and reducing noise.

- **Power Consumption**: A poorly designed clock tree can result in high power consumption due to excessive clock skew and unnecessary routing. A good clock tree minimizes power consumption by optimizing the clock distribution network.

- **Signal Integrity**: Clock signals are sensitive to noise and signal integrity issues. A well-designed clock tree minimizes signal distortion and ensures that the clock signal reaches all flip-flops with minimal distortion.

- **Timing Closure**: Meeting timing closure requirements is essential for the overall success of the chip design. A good clock tree design plays a critical role in achieving timing closure by minimizing clock skew and optimizing clock distribution.

### Lab Steps for Clock Tree Synthesis

- **Clock Root Buffer Insertion**: Inserting root buffers at the clock source helps to drive the clock signal efficiently through the clock tree. Root buffers also help in maintaining signal integrity and reducing clock skew.

- **Clock Distribution Network Synthesis**: The clock distribution network includes clock buffers and clock trees that distribute the clock signal to all sequential elements. This step ensures that the clock signal reaches all flip-flops with minimum skew.

- **Clock Tree Optimization**: Clock tree optimization involves balancing the clock tree, optimizing buffer placement, and minimizing clock skew. This step is crucial for meeting timing requirements and reducing power consumption.

- **Clock Tree Verification**: Once the clock tree synthesis is complete, it is essential to verify the clock tree using static timing analysis (STA) to ensure that timing requirements are met and there are no violations.
![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/a08e952b-1f61-4024-b3cc-ddfb4ca396d6)

- ![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/61ceede8-6e24-4232-bf0f-db79ad99efc1)

![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/05848815-4551-4ac2-9c1c-023e6aacd229)

![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/ef4f8956-20bb-47e1-ad32-821c1ada7d26)

![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/1e6f1411-04b5-4b65-a779-f4152adb2a5f)

![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/37a6e034-19d2-461e-9a2e-814e0b6eadab)

### Conclusion

A well-designed clock tree is essential for the overall performance and reliability of an ASIC design. By following best practices and utilizing advanced tools and methodologies, designers can achieve optimal clock distribution, minimize power consumption, and meet timing closure requirements, ultimately leading to a successful chip design.

# SKY130 DAY 5: Final Steps for RTL2GDS using TritonRoute and OpenSTA
## Routing and Design Check [DRC]
### Understanding Maze Routing and Lee's Algorithm
![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/897ecc74-2f63-4163-9f08-78a25e6eb338)

![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/d6c269bb-0752-4723-a81f-7d59f1262a7f)

![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/3dd3f9c6-8a59-4d00-9eba-bfb708c4e190)

![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/a4d7a4b6-aebc-469c-9acd-746df5a32ced)

![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/4dc1aad9-7872-4f12-b905-6079a975fab0)

Routing involves finding the most optimal path between two elements, such as clocks or flip-flops. Various routing algorithms exist, including the Steiner Tree algorithm and the Line Search algorithm. One notable algorithm is **Maze Routing**, specifically Lee's Algorithm (Lee 1961).

Consider connecting points 1 and 2 in the image below, where 1 is the source and 2 is the target. The goal is to find the shortest path between these points, minimizing zig-zags and favoring L-shaped routes. Lee's Algorithm is designed to search and connect these points efficiently, crucial for integrated circuit design.

### Steps in Lee's Algorithm

1. **Initialization:** Create a routing grid/matrix in the area to be routed, categorizing each cell into states like obstacle, empty, visited, source, or target.

2. **Wave Expansion:** Begin a wave expansion from the source cell, spreading out in all directions. At each step, examine neighboring cells and assign them a value one greater than the minimum value of their neighboring cells, excluding obstacles. Continue until the target cell is reached or no more cells can be visited.

3. **Backtracking and Path Reconstruction:** Once the target is reached, backtrack from the target to the source by following the cell values. This process may yield multiple paths, but the tool selects the one with fewer bends, providing the shortest route.

### Design Rule Check (DRC)

Routing not only connects points but must also adhere to specific rules. For example, rules dictate minimum distances between wires, minimum widths, pitch, and more. DRC cleaning ensures that routes can be fabricated and printed correctly in silicon.

### Power Distribution Network and Routing
#### Building the Power Distribution Network

1. Navigate to the openlane directory.
2. Run the command `docker` and then `./flow.tcl -interactive`. To acquire the openlane package, use `package require openlane 0.9`.
3. Prepare the design using `prep -design picorv32a -tag [folder name of run where cts had been done]`.
4. Generate the PDN using `gen_pdn`.

#### Power Straps to STD Cell Power

The power and ground rails have a pitch of 2.72µm, so the custom inverter cell also has a height of 2.72µm to ensure proper powering. All cells have the same height but varying widths.

![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/996e0035-7b54-41ab-9d07-d3dfe0c85572)

![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/2446ce37-45f0-4523-893c-3b3e29b8d0b3)

![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/924e5d75-5372-41d2-a001-f1c5fcc8b428)

### Basics of Global and Detail Routing and Configuring TritonRoute

TritonRoute is used for routing through the `run_routing` command. The routing stage is critical and can be executed using open-source or commercial tools, divided into two phases:

- Global Route / Fast Route: Establishes the initial framework for routing paths.
- Detail Route: Finalizes paths to ensure proper connectivity and compliance with design constraints.

### TritonRoute Features
1. **Honors Pre-processed Route Guides:** Converts non-preferred routes into preferred routing guides, ensuring efficient routing.
2. **Inter-Guide Connectivity:** Utilizes vertical routing for M1, resulting in vertically oriented lines.
3. **Intra & Inter Layer Routing:** Ensures orderly routing operations from lower to upper layers.

### TritonRoute Method for Connectivity

The Mixed Integer Linear Programming (MILP) method is used to find the optimal solution to connect two access point clusters, ensuring minimal and optimal routing.

### Routing Topology Algorithm and Final Files Post Route

After running the `run_routing` command, both global and detail routing are completed, with DRC violations reduced to 0. The final GDSII file is ready for fabrication and can be viewed using MAGIC.


![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/09b33954-b27d-43eb-ac2a-a0d54ad0e8cb)


![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/9d1238d5-a9c4-4d93-96c1-45f8cfc0a396)


![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/98b11f13-7af4-4cd7-8094-a92a5ac198f8)


![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/6563bf51-fec3-40b6-8307-17791f7ca2b7)

### Parasitic Extraction

OpenLANE does not include a SPEF extraction tool, so a separate tool in the `/home/vsduser/Desktop/work/tools/SPEF_EXTRACTOR` directory is used. Follow these steps for extraction:

1. Go to the directory containing the SPEF extraction tool, which includes a Python file called `main.py` and LEF & DEF files.
2. Use the following command to create the SPEF file:

![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/841cbb4d-3b6a-4909-a28c-8bcccb499b97)


```bash
python3 main.py /home/vsduser/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/26-03_05-49/tmp/merged.lef  /home/vsduser/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/26-03_05-49/tmp/routing/picorv32a.def
```

The SPEF file will be saved in the same location as the DEF file: `/home/vsduser/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/26-03_05-49/tmp/routing`.

### GDSII File Extraction

The last stage involves extracting the GDSII file for fabrication using the `run_magic` command. This command streams the GDSII file located at `runs/26-03_05-49/results/magic/picorv32a.gds`. The GDSII file can then be opened and viewed using MAGIC.

This completes the final steps for RTL2GDS using TritonRoute and OpenSTA, culminating in the fabrication-ready GDSII file.
![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/36d703a9-e9d8-435b-989c-deb7d2524ac4)


![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/c3bb1a0a-a1fd-4626-b6ca-5d43685ef681)


![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/364078a0-fe52-44da-98cf-842bacd4f01e)

![image](https://github.com/HarryMonteno/Rishabh-TR-VSDIAT-AdvancedPhysicalDesignUsingOpenLANE/assets/88733631/41ceeff0-ad99-4050-bb76-26aa939d76d9)
