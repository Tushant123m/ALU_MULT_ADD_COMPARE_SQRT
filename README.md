Project Title
Pipelined Arithmetic Datapath Using Shared Functional Units on FPGA

Project Overview
This project implements a pipelined arithmetic datapath on an FPGA using Quartus schematic design. The datapath supports multiplication, addition, square root, comparison, and direct data loading using a single shared accumulator. The design focuses on efficient hardware utilization by separating narrow input operations from wide accumulation operations. A hobby plus skill development based project is designed.

The architecture demonstrates how multiple arithmetic operations can share common resources through a multiplexer controlled datapath, similar to real processor and DSP designs.

Architecture Description
The datapath consists of the following main blocks:

An 8 bit by 8 bit multiplier used for low complexity and high speed multiplication
A 32 bit adder used for accumulation and intermediate arithmetic operations
A 32 bit square root unit that operates on accumulated values
A comparator used for control and decision making
A 32 bit accumulator register that stores intermediate and final results
A multiplexer that selects which operation result is written back to the accumulator

Two different operand widths are intentionally used:

8 bit input buses are used for multiplication
32 bit input buses are used for addition, square root, comparison, and direct loading

This separation reduces hardware cost while maintaining numerical precision.

Data Flow Explanation
Input data enters the system either from memory or external inputs. Small width data is routed to the multiplier. The multiplication result is then extended to 32 bits and accumulated in the main register. The accumulator output is fed back to the adder, square root unit, and comparator. The multiplexer selects the appropriate result based on the control logic and updates the accumulator on the next clock cycle.

Key Design Concepts
Narrow multiply and wide accumulate architecture
Shared functional units with multiplexer based selection
Pipelined data flow using registers
Efficient FPGA resource utilization
Scalable and modular datapath structure

Design Tools
Quartus Prime Lite Edition
Block Diagram File based schematic design
Verilog and VHDL IP blocks

Applications
Digital signal processing pipelines
Multiply accumulate based computation
FPGA arithmetic accelerators
Educational datapath and processor design
