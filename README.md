# Traffic-Light Controller + MOD-N Counter

## Overview
A simple two-road traffic-light controller designed using Verilog HDL. A finite-state machine (FSM) controls the North-South (NS) and East-West (EW) signals. A counter measures the duration of each signal phase.

## Signal sequence
1. NS green, EW red
2. NS yellow, EW red
3. NS red, EW green
4. NS red, EW yellow
5. Repeat

## Files
- `traffic_light_controller.v` — main FSM-based traffic controller
- `mod_n_counter.v` — reusable parameterized MOD-N counter
- `tb_traffic_light_controller.v` — simulation testbench
- `Design_Document.pdf` — project design document

## Tools
Any Verilog simulator can be used, such as Icarus Verilog with GTKWave, or a suitable FPGA design suite.

## Example simulation (Icarus Verilog)
```bash
iverilog -g2012 -o sim traffic_light_controller.v tb_traffic_light_controller.v
vvp sim
```
The testbench uses shortened phase durations to make the sequence visible quickly.

## Important note
This is an educational simulation design, not a certified road-traffic control device. Real installations require fail-safe hardware, verified timing, pedestrian handling, sensors, and applicable safety standards.
