# PCIe Gen6 SerDes PHY Receiver Front-End (CTLE Design)

An analog and mixed-signal integrated circuit design repository containing the LaTeX source files, custom document class, and high-resolution layout/simulation plots for a senior graduation thesis. This project details the design, implementation, layout, and corner simulation verification of a high-speed Continuous Time Linear Equalizer (CTLE) targetting the PCIe Gen6 standard (64 GT/s, PAM4).

This project was developed under the Electronics and Communications Engineering Department at the Faculty of Engineering, Ain Shams University (ASU), and proudly sponsored by **MediaTek**.

## 📑 Project Overview

As data rates scale up to 64 GT/s under the PCIe Gen6 standard, signal attenuation and Inter-Symbol Interference (ISI) across high-loss backplane channels present profound signal integrity challenges. To mitigate these effects, this thesis focuses on the receiver (RX) analog front-end, detailing a custom-designed, multi-stage **Continuous Time Linear Equalizer (CTLE)** optimized across PVT corners.

### Key Technical Contributions (CTLE Design)
* **Architecture Selection:** Comparative implementation and analysis of active, passive-inductor, asymmetrical-feedback, and source-degenerated topologies.
* **Tunability:** Implementation of high-precision resistor and capacitor banks for fine programmable gain peaking and boost frequency control.
* **Layout & Parasitic Extraction (PEX):** Completed full custom custom transistor-level layout, including optimization of floorplanning, floorplane matching, and post-layout PEX simulations to verify stability and bandwidth degradation.
* **Performance Indicators:** Comprehensive evaluation of AC response, 1dB compression points (linearity), eye-diagram optimization (for PAM4 signaling), pnoise tracking, and PVT robustness.

---

## 📁 Repository Structure

The repository is organized cleanly into functional sub-directories to manage the document sections and graphical assets seamlessly:

```text
├── Appendices/             # Appendix source documents (e.g., derivations, specs)
├── Chapters/               # Primary thesis text organized by component
│   ├── CTLE_parts/         # Focus area: Topology analysis, schematics, and PEX results
│   ├── DFE_parts/          # Architecture, algo theory, and comparator implementation
│   ├── Input_network_parts/# Input network termination and architecture
│   └── ...                 # Master chapter files (Chapter1.tex to Chapter6.tex)
├── frontmatter/            # Preliminary pages (Abstract, Cover, CV, Summary, Committee)
├── img/                    # High-resolution simulation plots and schematics
│   ├── CTLE_img/           # AC responses, layout floorplans, PVT sweeps, eye diagrams
│   ├── DFE_img/            # Loop timing graphs, latch topologies, behavioral sims
│   └── Termination_VGA_img/# Impedance matching networks, T-coils, and VGA tunings
├── Logo/                   # Institutional university vector logos
├── styling/                # Custom formatting stylesheets (.sty files)
├── Thesis.cls              # Master document class defining university specifications
├── Thesis.tex              # Master LaTeX entry point
└── Bibliography.bib        # BibTeX reference database
