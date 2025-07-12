PCIe Protocol Pipeline – RTL + DV Projects

This repository contains a connected set of RTL Design + SystemVerilog Verification projects that together simulate a PCIe data path: from FIFO buffering to Physical Layer decoding and TLP parsing with MMIO interface.

🔧 Project Structure

pcie_protocol_pipeline/

├── 01_SmartFIFO/

│   ├── rtl/

│   ├── tb/

│   ├── doc/

│   ├── sim/

│   └── README.md

│

├── 02_PCIe_PHY_Decoder/

│   ├── rtl/

│   ├── tb/

│   ├── doc/

│   ├── sim/

│   └── README.md

│

├── 03_PCIe_TLP_Decoder/

│   ├── rtl/

│   ├── tb/

│   ├── doc/

│   ├── sim/

│   └── README.md

│

├── dut_top/

│   ├── rtl/

│   ├── tb/

│   └── waveform/

│

├── shared_libs/

│   ├── packages/

│   ├── sv_interfaces/

│   └── macros/

│

├── scripts/

├── waveform_dumps/

├── Makefile

└── README.md


## 📁 Projects



### 🔹 1. SmartFIFO – Parametric Synchronous FIFO  

**Folder:** `01_SmartFIFO/`  

Designs a configurable FIFO in Verilog with SystemVerilog assertions and coverage. Used as a buffer between modules in the PCIe pipeline.



---



### 🔹 2. PCIe PHY Decoder – 8b/10b + Lane Deskew  

**Folder:** `02_PCIe_PHY_Decoder/`  

Implements PCIe physical layer decoder (Gen1-style). Includes 8b/10b decoding, disparity checking, comma detection, and lane deskew.



---



### 🔹 3. PCIe TLP Decoder – Transaction Layer + MMIO  

**Folder:** `03_PCIe_TLP_Decoder/`  

Parses PCIe TLP packets and maps them to a register interface using MMIO-style decoding. Simulates endpoint behavior in SoCs.



---



## 📦 Integration



- `dut_top/`: Integration testbench for FIFO → PHY → TLP

- `shared_libs/`: Common packages, SV interfaces, macros

- `scripts/`: Stimulus generators and helpers

- `waveform_dumps/`: Store `.vcd`, `.fst`, and waveform snapshots



---



## 🛠 Tools Used



- Verilog / SystemVerilog / SVA

- Icarus Verilog / ModelSim / GTKWave

- Python (for scripts)

- Git & GitHub



---



## 🧠 Skills Demonstrated



- RTL Design (FSMs, parameterization, pipelines)

- Protocol-level design (PCIe physical + transaction layer)

- SystemVerilog Verification (testbenches, assertions, coverage)

- Modular project structuring and reuse



---



## 👨‍💻 Author



**Pradeep M Navalagi**  

M.Tech – VLSI Design & Embedded Systems  

RVCE, Bangalore
