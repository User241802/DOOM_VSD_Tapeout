# Day 0 - Task 0: Tool Installation Setup

## 📅 Date: September 19, 2025
## 🎯 Task: Install Yosys, Iverilog, and GTKWave

## 🎯 Objectives
**What was planned:**
- Set up Ubuntu 20.04+ environment with required system specifications (6GB RAM, 50GB HDD, 4vCPU)
- Install **Yosys** (Open-source synthesis tool) from source using build dependencies
- Install **Iverilog** (Icarus Verilog simulator) via package manager
- Install **GTKWave** (Waveform viewer) for signal analysis
- Verify successful installation of all three tools
- Document the installation process and create tool snapshots for GitHub repository

---

## ✅ Achievements  
**What was completed:**

### System Preparation
- [x] Verified system requirements: Ubuntu 20.04+ with adequate resources
- [x] Updated package repositories using `sudo apt-get update`
- [x] Ensured stable internet connection for downloads

### Yosys Installation (Source Build)
- [x] Cloned Yosys repository from GitHub: `git clone https://github.com/YosysHQ/yosys.git`
- [x] Installed essential build dependencies:
  - `build-essential clang bison flex`
  - `libreadline-dev gawk tcl-dev libffi-dev git`
  - `graphviz xdot pkg-config python3`
  - `libboost-system-dev libboost-python-dev libboost-filesystem-dev zlib1g-dev`
- [x] Configured build environment: `make config-gcc`
- [x] Successfully compiled Yosys: `make`
- [x] Installed system-wide: `sudo make install`
  <img width="939" height="645" alt="image" src="https://github.com/user-attachments/assets/a690a1f1-7036-46c0-8ad8-b7713910ee5c" />


### Iverilog Installation
- [x] Updated package list: `sudo apt-get update`
- [x] Installed Iverilog: `sudo apt-get install iverilog`
- [x] Verified installation with version check
<img width="939/2" height="634/2" alt="image" src="https://github.com/user-attachments/assets/270f07e5-39f8-489c-8741-aecfd880eaf1" />

### GTKWave Installation
- [x] Updated package repositories
- [x] Installed GTKWave: `sudo apt install gtkwave`
- [x] Confirmed GUI accessibility
<img width="798/2" height="91/2" alt="image" src="https://github.com/user-attachments/assets/1a6a1be9-9a55-4cb6-96a8-d6fa376a4126" />


### Documentation
- [x] Captured tool installation screenshots
- [x] Documented command sequences and outputs
- [x] Created initial GitHub repository structure

---

## 🚧 Challenges
**Issues encountered and solutions:**

Luckily, I was able to install everything without any difficulties.

---

## 📚 Learnings
**Key technical insights:**

### Tool Ecosystem Knowledge
- **Yosys**: Open-source synthesis tool that converts RTL to gate-level netlists
- **Iverilog**: Standards-compliant Verilog simulator for functional verification
- **GTKWave**: Essential for debugging through waveform analysis
- **Integration**: These tools form a complete open-source digital design flow

### System Administration
- **Package Management**: Effective use of `apt` for dependency resolution
- **Build Environment**: Importance of proper compiler toolchain setup
- **Environment Variables**: How tool installation affects system PATH

### RISC-V Ecosystem Context
- These tools provide the foundation for open-source RISC-V development
- Understanding the complete toolchain from RTL to silicon
- Preparation for industry-standard EDA tool integration later in the program

---

## 🔧 System Configuration

**Environment Details:**
- **OS**: Ubuntu 20.04+ LTS
- **RAM**: 6GB (minimum)
- **Storage**: 50GB HDD space
- **CPU**: 4 vCPU cores
- **VM**: Oracle VirtualBox (as recommended)



---

*This completes Day 0 - Task 0 of the RISC-V Chip Tapeout Program. Ready to proceed with next ones.*
