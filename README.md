Project Title

Pipelined Arithmetic Datapath using Shared Functional Units (Quartus / FPGA)

Overview

This project implements a shared, pipelined arithmetic datapath on FPGA using Quartus schematic design. The datapath supports multiplication, addition, square root, comparison, and direct load operations using a single accumulator and a MUX-controlled feedback path. The design demonstrates efficient hardware resource utilization through narrow multiply and wide accumulate architecture.

Architecture Description

The datapath consists of:

8-bit × 8-bit Multiplier for low-resource, high-speed multiplication

32-bit Adder for accumulation and intermediate results

32-bit Square Root unit operating on accumulated values

Comparator for control decisions

32-bit Accumulator Register

MUX-based result selection

Two operand widths are used:

8-bit buses (A8, B8) → multiplication stage

32-bit buses (A32, B32) → add, sqrt, compare, and load operations

This separation allows optimized multiplication while preserving precision during accumulation.

Dataflow

External/RAM data enters through 8-bit inputs

Multiplier produces a 16-bit result

Result is extended and accumulated into 32-bit register

Accumulator feeds ADD, SQRT, or Comparator

MUX selects the next accumulator value

Key Design Concepts

Narrow multiply, wide accumulate (DSP-style architecture)

Resource-efficient FPGA design

MUX-controlled shared datapath

FSM-friendly structure

Scalable bit-widths

Tools Used

Quartus Prime Lite Edition

Block Diagram File (BDF)

Verilog/VHDL IP blocks

Applications

DSP pipelines

MAC-based computation

FPGA arithmetic accelerators

Educational processor/datapath design
