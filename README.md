# SYNAPSE

A custom SoC for recording and stimulating nerve/muscle signals through shared electrodes.
Built for SoC Labs on the nanoSoC reference design (Arm Cortex-M0).

## Why
Closed-loop nerve interfaces need recording and stimulation on the same electrodes, with
tight timing between them. SYNAPSE puts both on one chip, coordinated by a small
Trigger/Sync FSM and controlled by a Cortex-M0.

## Architecture
- Cortex-M0 + DMA, SWD debug
- Analog FSM / Trigger-Sync
- Record path: TIA, PGA, SAR/ΔΣ ADCs
- Stim path: pulse generator, current DAC, limiter
- 4-electrode switch shared by both paths

See `docs/` for the block diagram.

## Layout
- `rtl/`   Verilog sources
- `models/` behavioural models
- `tb/`    testbenches
- `docs/`  diagrams and notes

## Status
Early development: architecture done, FSM and Trigger/Sync RTL next.

## SoC Labs
Project page: <paste your soclabs.org project URL here>
