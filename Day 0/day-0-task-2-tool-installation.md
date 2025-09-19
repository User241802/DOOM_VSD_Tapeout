# Day 0 - Task 1: Tool Installation Setup

## 📅 Date: September 19, 2025
## ⏰ Duration: Full Day
## 🎯 Task: Install Yosys, Iverilog, and GTKWave

---

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

### Iverilog Installation
- [x] Updated package list: `sudo apt-get update`
- [x] Installed Iverilog: `sudo apt-get install iverilog`
- [x] Verified installation with version check

### GTKWave Installation
- [x] Updated package repositories
- [x] Installed GTKWave: `sudo apt install gtkwave`
- [x] Confirmed GUI accessibility

### Documentation
- [x] Captured tool installation screenshots
- [x] Documented command sequences and outputs
- [x] Created initial GitHub repository structure

---

## 🚧 Challenges
**Issues encountered and solutions:**

### Challenge 1: Yosys Build Dependencies
**Issue:** Initial compilation failed due to missing development packages
**Solution:** Systematically installed all required dependencies as specified in installation guide. Used `sudo apt install make` separately when make was not found.

### Challenge 2: Compilation Time
**Issue:** Yosys source compilation took longer than expected (~45 minutes)
**Solution:** Ran compilation in background while proceeding with other tool installations. Monitored progress using `htop` to ensure system resources were adequate.

### Challenge 3: Path Configuration
**Issue:** After installation, tools were not immediately accessible from command line
**Solution:** Verified installation paths and ensured `/usr/local/bin` was in system PATH. Opened new terminal session to refresh environment variables.

---

## 📚 Learnings
**Key technical insights:**

### Build System Understanding
- **Source vs Package Installation**: Learned the difference between installing from source (Yosys) vs package manager (Iverilog, GTKWave)
- **Dependency Management**: Understanding how build dependencies affect compilation success
- **Make System**: Gained experience with GNU Make configuration (`make config-gcc`) and installation processes

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

## ⏭️ Next Steps
**Plan for following day:**

### Immediate Actions (Day 1)
- [ ] **Tool Verification**: Create simple Verilog testbench to verify all tools work together
- [ ] **Workflow Testing**: Run complete simulation flow: Verilog → Iverilog → VCD → GTKWave
- [ ] **Repository Update**: Push installation documentation and tool screenshots to GitHub
- [ ] **Environment Setup**: Configure shell aliases and environment variables for efficient tool usage

### Technical Preparation
- [ ] **Study RISC-V ISA**: Begin understanding RISC-V instruction set architecture
- [ ] **Verilog Refresh**: Review SystemVerilog syntax and best practices
- [ ] **Tool Documentation**: Read Yosys, Iverilog, and GTKWave user manuals

### Program Preparation
- [ ] **Lab Environment**: Set up organized directory structure for upcoming lab work
- [ ] **Version Control**: Initialize proper Git workflow for design files
- [ ] **Collaboration Setup**: Prepare for integration with program-wide repositories

---

## 📊 Installation Summary

| Tool | Version | Installation Method | Status | Notes |
|------|---------|-------------------|--------|-------|
| Yosys | Latest (master) | Source Build | ✅ Successful | ~45 min compilation time |
| Iverilog | Package Default | apt package | ✅ Successful | Quick installation |
| GTKWave | Package Default | apt package | ✅ Successful | GUI verified |

---

## 🔧 System Configuration

**Environment Details:**
- **OS**: Ubuntu 20.04+ LTS
- **RAM**: 6GB (minimum)
- **Storage**: 50GB HDD space
- **CPU**: 4 vCPU cores
- **VM**: Oracle VirtualBox (as recommended)

**Tool Paths:**
- Yosys: `/usr/local/bin/yosys`
- Iverilog: `/usr/bin/iverilog`
- GTKWave: `/usr/bin/gtkwave`

---

*This completes Day 0 - Task 1 of the RISC-V Chip Tapeout Program. Ready to proceed with actual design work and verification workflows.*