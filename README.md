# TinyMIPS-ISA-Implementation

**Implementation of TinyMIPS in Verilog**

# Introduction

TinyMIPS is a simplified version of MIPS ISA which is a sort of Microprocessor

Instruction Set Architecture. TinyMIPS has small set of instructions defined in its ISA for performing basic arithmetic, logic, data transfer and memory operations. In this implementation project, we will deal with given instructions:

- Arithmetic and logic instructions: ADD, ADDi, MUL, SRL
- Memory instructions: LD, ST
- Data-Transfer instructions: CP, Cpi
- Program control instructions: BEQ, BLT, BGT

We will use a simple block of RAM (blram) for instruction and data storage in our code as a seperate module from main TinyMIPS module.

A special testing and developing environment used for this project. In order to make sure everything works well and synthesized correctly, we will also use EDA Playground for double-check.

- Design Environment: Xilinx ISE 14.7
- Simulation Environment: ISim Simulation Engine P.20131013 - Time Resolution for Simulation: 1ps.
- Verilog Modules Will be Compiled: 4 (TinyMIPS, blram, tb_TinyMIPS, glbl)
- Top Module: TinyMIPS.v
- Verilog Test Fixtures: tb_TinyMIPS.v
- clk: Clock Signal
- rst: Reset Signal

Each instruction in TinyMIPS ISA was implemented using case statement in always block which is sensitive to clock signal.
