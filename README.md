# RISC-V-SoC-Tapeout_Maaz_Week-2
SoCs design fundamentals and general understanding of BabySoC
# Understanding System-on-Chip (SoC) and the Role of BabySoC

<details><summary> What is a System-on-Chip (SoC)?</summary>

A **System-on-Chip (SoC)** is essentially a complete computing system integrated onto a single silicon chip. Instead of using separate components like a CPU board, memory modules, and peripheral chips, SoCs bring everything together into one compact package. This approach is widely used in smartphones, wearables, IoT devices, and embedded systems, where power efficiency, compact size, and high performance are essential.

An SoC can be thought of as a miniature motherboard — but everything, from the processor to communication interfaces, lives on one integrated circuit.

</details>

<details><summary> Core Components of a Typical SoC</summary>

A standard SoC integrates multiple functional blocks that work together to execute applications efficiently:

### 1. CPU (Central Processing Unit)
The CPU is the brain of the chip. It runs instructions, handles computations, and manages control signals for the entire SoC. Modern SoCs often use RISC-V, ARM, or proprietary cores depending on application requirements.

### 2. Memory
- **Volatile Memory (RAM)**: Temporary storage for active data and instructions.  
- **Non-Volatile Memory (ROM/Flash)**: Holds firmware, bootloaders, or permanent data.  

This integration reduces latency between computation and storage compared to using external memory modules.

### 3. Peripherals & I/O Interfaces
Peripherals allow the SoC to communicate with the outside world—such as UART, SPI, I²C, USB, GPIO, or specialized accelerators. I/O ports connect to external sensors, displays, audio devices, or other chips.

### 4. Interconnect / Bus System
The interconnect is the communication backbone of the SoC. It connects CPU, memory, and peripherals through high-speed buses or network-on-chip (NoC) structures, ensuring synchronized data flow across all components.

Additional blocks like Graphics Processing Units (GPU), Digital Signal Processors (DSP), Power Management Units (PMU), and wireless interfaces (e.g., Wi-Fi, Bluetooth) may also be included depending on the SoC’s target use.

</details>

# Why BabySoC is a Simplified Model for Learning?
<details> <summary>BabySoC</summary>
  
**BabySoC (VSDBabySoC)** is a compact, educational RISC-V based SoC designed to simplify the learning curve of SoC design and verification. It integrates three core open-source components:

- **RVMYTH CPU** — A lightweight RISC-V core used for instruction execution and control.  
- **Phase-Locked Loop (PLL)** — Generates stable clock signals for synchronized operation.  
- **10-bit Digital-to-Analog Converter (DAC)** — Converts digital output to analog signals (e.g., for audio/video interfacing).

By focusing on essential building blocks rather than overwhelming complexity, BabySoC allows students and hobbyists to:

- Understand interactions between CPU, clocking, and peripherals.  
- Experiment with digital-to-analog interfacing in real designs.  
- Work with open-source IP cores in a fully documented environment.  
- Explore SoC design in the Sky130 technology node, bridging theory and practice.

This makes BabySoC ideal for first-time SoC designers who want to grasp core architectural principles before diving into industrial-scale designs.

</details>

## Role of Functional Modelling Before RTL and Physical Design

<details>
  <summary>Functional Modelling</summary>
  In a typical SoC design flow, functional modelling is the crucial first step, preceding RTL coding and physical implementation:

1. <h2>Functional Modelling</h2>  
   - Abstract, high-level description of SoC behavior (often using C/SystemC, or simple HDL behavioral models).  
   - Focuses on verifying what the system should do, not how it’s implemented.  
   - Allows early exploration of system architecture and component interactions without worrying about timing, area, or layout.
</details>
<details>
  <summary>RTL Design</summary>
2. <h2>RTL (Register-Transfer Level) Design</h2> 
   - Describes the actual hardware structure using Verilog or VHDL.  
   - Adds clocking, registers, and timing to the previously validated functional model.  
</details>
<details>
  <summary>Physical Design</summary>
3. <h2>Physical Design</h2>  
   - Translates RTL into actual silicon layouts (place and route).  
   - Deals with floorplanning, routing, clock tree synthesis, and timing closure.

For learners, starting with functional models provides a low-risk, high-feedback environment to experiment with architecture, debug data flow, and validate functionality early. BabySoC’s design encourages this approach by offering clear functional components, making the transition to RTL and then physical design more structured and understandable.

</details>

## Summary

System-on-Chip technology brings multiple subsystems together on one chip, enabling efficient, powerful, and compact devices. BabySoC distills these concepts into an accessible learning platform, where learners can understand CPU-peripheral interaction, clock synchronization, and analog interfacing—all within a manageable design size. Functional modelling plays a critical role in ensuring these systems work as intended before committing to RTL or silicon, making BabySoC a perfect educational bridge between theory and real chip design.
