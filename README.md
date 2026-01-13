# Full-Custom 65nm 8-bit Microprocessor - Supplementary Materials

Supplementary materials for the full-custom 8-bit microprocessor design project. Contains detailed verification results, layout screenshots, power analysis data, and test waveforms supporting the main technical paper.

**For complete technical documentation, methodology, and analysis, see [docs/vlsi_final_proj.pdf](docs/vlsi_final_proj.pdf)**

---

## Project Overview

**Title:** *Full-Custom 65nm 8-bit Microprocessor: Design Optimization and Timing Closure in Deep Sub-Micron Technology*

**Key Results:**
- Total chip area: 4,100 µm²
- Timing margin: 88.8% @ 100 MHz target
- Average parasitic degradation: 241% (pre/post-layout)
- Power consumption: 876 µW @ 1.0V, 25°C
- All components: DRC/LVS clean

**Architecture:**
- 8-bit ripple-carry ALU with 2's complement
- 8-bit logarithmic left shifter (3-stage)
- 8×8 SRAM with custom peripherals
- PLA-based control logic with 3 latches
- Two-phase clocking (Φ1/Φ2)

---

## Repository Contents

This repository provides **supplementary figures and verification data** that extend beyond what's included in the main paper. All materials are organized by component for easy reference.

### Structure
```
vlsi-microprocessor/
├── docs/
│   └── vlsi_final_proj.pdf          # Complete technical paper (primary documentation)
│
└── figures/
    ├── architecture/                # System-level diagrams
    ├── alu/                         # ALU schematics, layouts, verification
    ├── shifter/                     # Shifter implementation details
    ├── sram/                        # Memory system with peripherals
    ├── control/                     # Control logic subcomponents
    │   ├── pla/                     # PLA decode array
    │   ├── mux/                     # 3-input NAND multiplexer
    │   ├── latch/                   # D-latches (Φ1/Φ2)
    │   ├── bus_driver/              # Tri-state buffers
    │   └── shift_bypass/            # Bypass control logic
    └── integration/                 # Full-chip integration and testing
```

### What's Included

Each component directory contains:
- **Schematics** - Circuit topology and implementation
- **Layouts** - Physical implementation screenshots (NDA-compliant)
- **DRC/LVS Reports** - Physical verification results
- **Test Waveforms** - Functional verification screenshots
- **Timing Analysis** - Delay measurements (pre/post-layout if available)
- **Power Analysis** - Cadence Calculator results

**Additional materials beyond the paper:**
- Individual component verification waveforms
- Detailed DRC/LVS validation screenshots
- Cadence Calculator power analysis data
- Peripheral circuit implementations (decoder, precharge, drivers, buffers)
- Control logic subcomponent breakdown (PLA, mux, latches, bus drivers, bypass)
- Full instruction sequence test waveforms

---

## Quick Links

- **Main Paper:** [docs/vlsi_final_proj.pdf](docs/vlsi_final_proj.pdf)
- **Full Chip Layout:** [figures/architecture/](figures/architecture/)
- **System Datapath:** [figures/architecture/](figures/architecture/)
- **Critical Path Analysis:** [figures/full_integration/](figures/full_integration/)
- **Component Verification:** Available in each component's directory under [figures/](figures/)

---

## Design Methodology

**Technology:** 65nm CMOS  
**Tools:** Cadence Virtuoso (schematic/layout), Mentor Calibre (DRC/LVS/extraction), Cadence Spectre (simulation)  
**Approach:** Full-custom design with systematic minimum-sizing methodology (140nm NMOS baseline)

For detailed design decisions, transistor sizing rationale, critical path optimization strategies, and integration challenges, refer to the main paper.

---

## Academic Context

Completed as part of Columbia University's **Digital VLSI Design (EE4321)** course, Fall 2025. Demonstrates complete IC design flow from architecture specification through physical verification.

**Author:** Albert Wang  
**Institution:** Columbia University, Department of Electrical Engineering  
**Contact:** aw3741@columbia.edu

---

## NDA Notice

Layout GDS files and detailed DRC/LVS reports are not included in this repository due to NDA restrictions with the PDK provider. This repository contains only NDA-compliant supplementary materials (layout screenshots, schematics, test waveforms, and analysis data).

For access to confidential design files, contact aw3741@columbia.edu with appropriate verification of NDA status.

---

*For questions about the design methodology, technical details, or collaboration opportunities, please refer to the paper first, then contact via email.*