# Open Source Software Audit - Linux Kernel
**Student Name:** Akshat Kumar Singh  
**Reg Number:** 24BSA10101  
**Course Name:** Open Source Software  
**Chosen Software:** Linux Kernel  

## Project Overview
This project is an audit and exploration of the Linux Kernel, the foundation of the open-source ecosystem. It demonstrates a practical understanding of the Linux Kernel's open-source nature (licensed under GPL) and its footprint on a system. The repository includes a set of Bash shell scripts to audit the system, inspect FOSS packages, analyze logs, and dynamically generate an open-source manifesto.

## Directory Structure
```text
CF_DAILY/Scripts/
├── README.md                           # This file
├── system_identity.sh                  # Outputs basic Linux OS and user info
├── package_inspector.sh                # Checks for the Linux Kernel and other FOSS software
├── disk_auditor.sh                     # Scans directory sizes and permissions
├── log_analyzer.sh                     # Simple parser for finding keywords in logs
└── manifesto_generator.sh              # Interactive script to make a personalized manifesto
```

## Included Shell Scripts

### 1. System Identity Report (system_identity.sh)
Displays the current Linux distribution in use, kernel version, logged-in user details, and system uptime. It includes a brief note about Linux's GPL licensing.

### 2. FOSS Package Inspector (package_inspector.sh)
Checks if the Linux Kernel or chosen FOSS software is installed on the system using dpkg. It displays the installed version, status, and provides a quick overview.

### 3. Disk and Permission Auditor (disk_auditor.sh)
Loops over crucial Linux directories (like /etc, /var/log, /home) to report their size and permissions. It also uniquely checks /boot where kernel configs and images are stored.

### 4. Log File Analyzer (log_analyzer.sh)
A utility script that reads any log file line-by-line. Provide a log file and optionally a keyword (defaults to "error"). It returns the number of matches and the last few matching lines.

### 5. Open Source Manifesto Generator (manifesto_generator.sh)
An interactive script. It asks you a few simple questions about your tech interests and generates a customized text file (manifesto_<username>.txt) detailing your personal open-source philosophy.

## How to Run the Scripts on Ubuntu/Linux

**Step 1: Make scripts executable**  
Before running any script for the first time, you must give it execute permissions:

```bash
chmod +x *.sh
```

**Step 2: Execute the scripts**  
Run each script using `./`:

```bash
./system_identity.sh
./package_inspector.sh
./disk_auditor.sh
./log_analyzer.sh /var/log/syslog "error"
./manifesto_generator.sh
```

## Dependencies
* A standard Linux environment (Ubuntu/Debian recommended)
* Bash shell
* Standard pre-installed utilities: awk, du, grep, dpkg (for Debian-based distros)

Created for the Open Source Software capstone assignment.
