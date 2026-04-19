# ⚡ Multi-Output Power Supply Board — KiCad Project

A multi-output DC power supply board that takes 12V input and outputs three regulated voltages simultaneously.

## Overview

This board is designed to power multiple components or modules at different voltage levels from a single 12V DC source (via an external wall adapter). Instead of using separate power supplies for each device, this board provides 12V, 5V, and 3.3V outputs all at once.

## How It Works

```
Wall Outlet (220V AC)
        ↓
External 12V DC Adapter (sold separately)
        ↓
This Board
        ↓
┌───────────────────────┐
│  12V ── high power    │
│   5V ── Arduino, etc. │
│  3.3V ── ESP32, etc.  │
└───────────────────────┘
```

## Components

| Reference | Component | Purpose |
|---|---|---|
| J1 | Barrel Jack (DC input) | 12V input from wall adapter |
| U1 | LM7805 | Regulates 12V → 5V |
| U2 | LM317 | Regulates 12V → 3.3V |
| C1–C4 | Capacitors | Smooth and stabilize voltage outputs |
| D1 | LED | Power indicator light |
| R1 | Resistor | Current limiting for indicator LED |
| S1 | Slide Switch (EG1218) | Master on/off switch |
| J2–J4 | Screw Terminals / Connectors | Output connections for each voltage |

## Nets

| Net Name | Description |
|---|---|
| `12V` | Direct input voltage |
| `5V` | Regulated 5V output |
| `3.3V` | Regulated 3.3V output |
| `GND` | Common ground |
| `PWR_input` | Input power rail |
| `PWR_output` | Output power rail |

## PCB Layout

- All components placed on **F.Cu**
- Through-hole components for easy hand soldering
- Standard trace widths

## Files

| File | Description |
|---|---|
| `second.kicad_sch` | Schematic |
| `second.kicad_pcb` | PCB layout |
| `second.kicad_pro` | KiCad project file |

## What You Need

- This PCB (manufactured or on breadboard)
- A **12V DC wall adapter** with a barrel jack connector (not included)
- Soldering iron + solder

## Tools Used

- [KiCad](https://www.kicad.org/) — schematic and PCB design

## Status

- [x] Schematic complete
- [x] PCB layout complete
- [ ] Gerbers generated
- [ ] Manufactured & tested
