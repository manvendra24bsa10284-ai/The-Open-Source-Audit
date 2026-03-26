cat << 'EOF' > README.md
# 🐧 The Open Source Audit — Linux Kernel

<div align="center">

![Linux](https://img.shields.io/badge/Linux-Kernel-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![License](https://img.shields.io/badge/License-GPL--v2-blue?style=for-the-badge)
![Course](https://img.shields.io/badge/Course-OSS%20NGMC-navy?style=for-the-badge)
![VIT](https://img.shields.io/badge/Institution-VIT-red?style=for-the-badge)
![Bash](https://img.shields.io/badge/Shell-Bash-4EAA25?style=for-the-badge&logo=gnubash&logoColor=white)

</div>

---

## 👤 Student Details

| Field | Details |
|---|---|
| **Name** | Manvendra Singh Shah |
| **Registration No** | 24BSA10284 |
| **Slot** | f11 |
| **Course** | Open Source Software (OSS NGMC) |
| **Institution** | VIT Bhopal |
| **Software Chosen** | Linux Kernel |
| **License** | GNU General Public License v2 (GPL-2.0) |

---

## 📌 About This Project

This capstone project for the Open Source Software (OSS NGMC) course at VIT provides a comprehensive audit of the Linux Kernel alongside practical command-line implementations.

**Key Components:**
* **Structured Audit:** An in-depth analysis of the Linux Kernel's origins, GPL v2 licensing, ethical foundations, technical footprint, and its broader role in the FOSS ecosystem.
* **Bash Scripting Portfolio:** Five custom shell scripts demonstrating core Linux command-line proficiencies, including variables, control structures (loops/conditionals), file manipulation, and user input handling.

---

## 📁 Repository Structure

```text
The-Open-Source-Audit/
│
├── README.md               ← You are here
├── .gitignore
│
├── scripts/
│   ├── script1_system_identity.sh      ← System Identity Report
│   ├── script2_package_inspector.sh    ← FOSS Package Inspector
│   ├── script3_disk_permission_audit.sh    ← Disk & Permission Auditor
│   ├── script4_log_analyzer.sh         ← Log File Analyzer
│   └── script5_manifesto_generator.sh      ← Manifesto Generator
│
├── # ... (previous tree structure)
├── report/
│   └── OSS_Audit_Report_ManvendraSinghShah_24BSA10284.pdf
│
└── screenshots/
    └── (script output screenshots)
``` 

⚡ Quick Start — Run All Scripts
# ...
    # 1. Make all scripts executable at once
chmod +x scripts/*.sh

# 2. Run each script
./scripts/script1_system_identity.sh
./scripts/script2_package_inspector.sh
./scripts/script3_disk_permission_audit.sh
./scripts/script4_log_analyzer.sh /var/log/syslog error
./scripts/script5_manifesto_generator.sh

<div align="center">

Submitted as part of the Open Source Software (OSS NGMC) Capstone Project — VIT Bhopal

Manvendra Singh Shah | 24BSA10284 | Slot: f11

</div>
EOF

cat << 'EOF' > scripts/script1_system_identity.sh
#!/bin/bash
echo "=================================================="
echo "  Open Source Audit — Manvendra Singh Shah"
echo "  Roll No : 24BSA10284"
echo "  Slot    : f11"
echo "  Software: Linux Kernel"
echo "=================================================="
echo ""
echo "Distribution : $(grep PRETTY_NAME /etc/os-release | cut -d '"' -f 2)"
echo "Kernel       : $(uname -r)"
echo "User         : $(whoami)"
echo "Home Dir     : $HOME"
echo "Uptime       : $(uptime -p)"
echo "Date/Time    : $(date)"
echo ""
echo "--------------------------------------------------"
echo "OS License   : GNU General Public License v2 (GPL-2.0)"
echo "This means   : You are free to run, study, share,"
echo "               and modify this operating system."
echo "--------------------------------------------------"
EOF

cat << 'EOF' > scripts/script5_manifesto_generator.sh
#!/bin/bash
echo "=================================================="
echo "  Open Source Manifesto Generator"
echo "  Powered by: Bash + your own thinking"
echo "=================================================="
echo ""
echo "Answer three questions and I will write your manifesto."
echo ""
read -p "1. Name one open-source tool you use every day: " tool
read -p "2. In one word, what does 'freedom' mean to you? " freedom
read -p "3. Name one thing you would build and share freely: " build
echo ""
echo "Generating your manifesto..."
echo ""

filename="manifesto_Manvendra.txt"

cat << MANIFESTO > $filename
MY OPEN SOURCE MANIFESTO Generated on: $(date) By: Manvendra Singh Shah (24BSA10284)
I believe in the power of open source.

Every day I rely on $tool — a tool built by the community,
for the community, and given freely to the world.
It exists because someone chose to share rather than to lock away.

To me, freedom means $freedom.
That is exactly what open-source software protects —
not just the freedom to use a program, but the freedom to understand it,
improve it, and pass it on to someone else.

One day I will build $build and share it freely with the world.
Because knowledge shared is knowledge multiplied.
Every great tool I use today exists because someone before me chose to share their work.

I stand on the shoulders of giants — Linus Torvalds, Richard Stallman,
and the thousands of unnamed contributors who wrote code at night
for no pay and no recognition, only the belief that it mattered.

I carry that responsibility forward.

— Manvendra Singh Shah, $(date '+%A, %d %B %Y')
MANIFESTO

echo "Manifesto saved to: $filename"
echo "--------------------------------------------------"
cat $filename
EOF