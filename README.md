# PCIe Protocol Pipeline – RTL + DV Projects

This repository contains a connected set of RTL Design + SystemVerilog Verification projects that together simulate a PCIe data path: from FIFO buffering to Physical Layer decoding and TLP parsing with MMIO interface.

---

## 🔧 Project Structure

```
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
```

---

## 📁 Projects

### 🔹 1. SmartFIFO – Parametric Synchronous FIFO

**Folder:** `01_SmartFIFO/`

* Configurable FIFO with parameterized depth and thresholds
* RTL written in Verilog
* Verified using SystemVerilog testbench and SVA
* Acts as a data buffer for downstream PHY and TLP modules

📌 **Use Case**: Common in memory controllers, AXI stream buffers, PCIe lanes.

---

### 🔹 2. PCIe PHY Decoder – 8b/10b + Lane Deskew

**Folder:** `02_PCIe_PHY_Decoder/`

* Implements the PCIe Physical Layer decoding logic (Gen1-style)
* Includes 8b/10b decoder, comma aligner, disparity checker, and lane deskew
* Simulates a 2-lane input stream
* Verified using directed and random symbol sequences

📌 **Use Case**: Common in PCIe PHY IPs, serializers/deserializers, high-speed protocol bridges.

---

### 🔹 3. PCIe TLP Decoder – Transaction Layer + MMIO

**Folder:** `03_PCIe_TLP_Decoder/`

* Parses Transaction Layer Packets from decoded PHY output
* Decodes memory write/read packets and performs register mapping
* Implements a simple MMIO-style interface to simulate endpoint logic
* Includes SystemVerilog TB with packet driver, monitor, checker

📌 **Use Case**: Common in PCIe IPs, SoC peripheral interfaces, root-complex emulation.

---

## 📦 Integration

* `dut_top/`: Integration testbench for FIFO → PHY → TLP
* `shared_libs/`: Common packages, SV interfaces, macros
* `scripts/`: Stimulus generators and helpers
* `waveform_dumps/`: Store `.vcd`, `.fst`, and waveform snapshots

---

## 🛠 Tools Used

* Verilog / SystemVerilog / SVA
* Icarus Verilog / ModelSim / GTKWave
* Python (for scripts)
* Git & GitHub

---

## 🧠 Skills Demonstrated

* RTL Design (FSMs, parameterization, pipelines)
* Protocol-level design (PCIe physical + transaction layer)
* SystemVerilog Verification (testbenches, assertions, coverage)
* Modular project structuring and reuse
* End-to-end IP subsystem simulation

---

## 👨‍💻 Author

**Pradeep M Navalagi**
M.Tech – VLSI Design & Embedded Systems
RVCE, Bangalore



