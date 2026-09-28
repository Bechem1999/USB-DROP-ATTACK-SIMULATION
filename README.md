# 🔐 SQROCK IT Solution — Cybersecurity Internship

# Day 8: USB Drop Attack Simulation — Lab Only

![Kali Linux](https://img.shields.io/badge/Kali_Linux-2026.2-557C94?logo=kalilinux\&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.13.12-3776AB?logo=python\&logoColor=white)
![USB Security](https://img.shields.io/badge/USB-Security-orange)
![Cybersecurity](https://img.shields.io/badge/Cybersecurity-Training-red)
![Social Engineering](https://img.shields.io/badge/Social_Engineering-Awareness-blue)
![Endpoint Security](https://img.shields.io/badge/Endpoint-Security-green)
![Python Scripting](https://img.shields.io/badge/Python-Scripting-yellow)
![Ethical Hacking](https://img.shields.io/badge/Ethical-Hacking-purple)
![Lab Only](https://img.shields.io/badge/Environment-Local_Lab-lightgrey)

---

## 📌 Project Overview

As part of **Day 8 of the SQROCK IT Solution Cybersecurity Internship**, this project focuses on understanding the security risks associated with **USB drop attacks** and the importance of user awareness and endpoint security.

A USB drop attack is a social engineering technique in which an attacker intentionally leaves a USB storage device where a target may find it. The attacker relies on curiosity or trust to persuade the individual to connect and execute content from the device.

For this controlled laboratory exercise, a **benign Python payload** was created to demonstrate what could happen when an untrusted file is executed from removable media.

The program does **not** perform malicious actions. It only records basic system information such as:

* Timestamp
* Hostname
* Operating system
* Operating system version
* Current user
* Current working directory

The exercise was performed manually inside an authorized cybersecurity laboratory environment.

---

## 🎯 Objectives

The main objectives of this project were to:

* Understand the concept of USB drop attacks.
* Study the social engineering principles behind USB-based attacks.
* Understand why unknown USB devices can present security risks.
* Create a benign Python payload for awareness training.
* Demonstrate basic system-information collection.
* Observe the information that a seemingly harmless script can access.
* Understand the security implications of executing unknown files.
* Explore defensive measures against malicious USB devices.
* Strengthen Python scripting and Linux command-line skills.
* Practice ethical and controlled cybersecurity testing.

---

## 🛠️ Tools and Technologies Used

| Tool / Technology            | Purpose                                           |
| ---------------------------- | ------------------------------------------------- |
| **Kali Linux 2026.2**        | Cybersecurity laboratory environment              |
| **Python 3.13.12**           | Development of the benign awareness payload       |
| **Python `platform` module** | Collecting operating-system information           |
| **Python `socket` module**   | Retrieving hostname information                   |
| **Python `datetime` module** | Recording execution time                          |
| **Python `os` module**       | Retrieving user and working-directory information |
| **Terminal**                 | Running the Python script                         |
| **Nano**                     | Creating and editing project files                |
| **Git & GitHub**             | Version control and documentation                 |

---

## 🧠 Skills Demonstrated

* USB security awareness
* Social engineering analysis
* Endpoint security awareness
* Python programming
* Python standard libraries
* System-information gathering
* Linux command-line usage
* Security logging
* Threat modeling
* Defensive cybersecurity
* Security documentation
* Ethical hacking principles

---

## 🔬 Understanding USB Drop Attacks

A USB drop attack uses a physical USB device as a delivery mechanism for social engineering.

A typical attack scenario may involve:

```text
Unknown USB Device
        │
        ▼
Victim Finds Device
        │
        ▼
Curiosity / Trust
        │
        ▼
Device Connected
        │
        ▼
File Executed
        │
        ▼
Potential Security Impact
```

The important security lesson is that the **human decision to trust and execute unknown content** can become the initial point of compromise.

---

## 🧪 Methodology

The project was carried out through the following stages.

### Step 1 — Study USB Drop Attacks

The first stage involved studying how attackers may use USB devices as a social engineering mechanism.

The main focus was on:

* User curiosity
* Physical access
* Trust exploitation
* Unknown removable media
* Malicious or suspicious files
* Endpoint security

---

### Step 2 — Create the Project Directory

The Day 8 project directory was created inside the SQROCK internship workspace.

```bash
mkdir -p ~/sqrock-internship/day8-usb-drop
cd ~/sqrock-internship/day8-usb-drop
```

---

### Step 3 — Verify the Python Environment

The Python installation was verified:

```bash
python3 --version
```

Expected environment:

```text
Python 3.13.12
```

---

### Step 4 — Create a Benign Payload

A Python script was created using `nano`:

```bash
nano usb_awareness.py
```

The script was designed strictly for awareness training.

It records basic information about the system when manually executed.

---

## 💻 Python Implementation

The project uses Python's standard libraries:

```python
import platform
import socket
from datetime import datetime
import os
```

The script collects non-sensitive system information and writes the results to a local log file.

Example structure:

```python
import platform
import socket
from datetime import datetime
import os

timestamp = datetime.now()

hostname = socket.gethostname()
operating_system = platform.system()
os_version = platform.version()
username = os.getlogin()
current_directory = os.getcwd()

with open("recon_log.txt", "w") as log:
    log.write("USB Security Awareness Simulation\n")
    log.write("---------------------------------\n")
    log.write(f"Timestamp: {timestamp}\n")
    log.write(f"Hostname: {hostname}\n")
    log.write(f"Operating System: {operating_system}\n")
    log.write(f"OS Version: {os_version}\n")
    log.write(f"User: {username}\n")
    log.write(f"Working Directory: {current_directory}\n")
```

> **Safety note:** This implementation is intentionally benign. It does not establish persistence, modify system settings, execute additional commands, access credentials, or automatically run from a USB device.

---

## ▶️ Running the Awareness Simulation

The script was executed manually from the terminal:

```bash
python3 usb_awareness.py
```

After execution, the generated log can be viewed with:

```bash
cat recon_log.txt
```

The output contains information similar to:

```text
USB Security Awareness Simulation
---------------------------------
Timestamp: 2026-09-28 ...
Hostname: kali
Operating System: Linux
OS Version: ...
User: kali
Working Directory: /home/kali/sqrock-internship/day8-usb-drop
```

The exact values depend on the laboratory system on which the script is executed.

---

## 📊 Information Collected

| Information       | Purpose                                      |
| ----------------- | -------------------------------------------- |
| Timestamp         | Records when the script was executed         |
| Hostname          | Demonstrates basic device identification     |
| Operating System  | Demonstrates OS identification               |
| OS Version        | Demonstrates system-version identification   |
| Username          | Demonstrates local user context              |
| Working Directory | Demonstrates the script's execution location |

No passwords, browser credentials, API keys, tokens, private files, or other sensitive authentication information were collected.

---

## 🧪 Laboratory Environment

The exercise was conducted in a controlled Kali Linux environment.

```text
Operating System : Kali Linux 2026.2
Python           : 3.13.12
Environment      : Authorized Cybersecurity Lab
Execution        : Manual
Payload Type     : Benign Python Awareness Script
Persistence      : None
Autorun          : None
External Target  : None
```

### Laboratory Architecture

```text
┌────────────────────────────────────┐
│         Kali Linux 2026.2         │
│                                    │
│   ┌────────────────────────────┐   │
│   │  USB Awareness Simulation  │   │
│   │       Python Script        │   │
│   └──────────────┬─────────────┘   │
│                  │                 │
│                  ▼                 │
│   ┌────────────────────────────┐   │
│   │ Basic System Information   │   │
│   │       Collection           │   │
│   └──────────────┬─────────────┘   │
│                  │                 │
│                  ▼                 │
│   ┌────────────────────────────┐   │
│   │      recon_log.txt         │   │
│   │       Local Output         │   │
│   └────────────────────────────┘   │
└────────────────────────────────────┘
```

---

## ⚙️ Environment Configuration

The project was created using:

```bash
mkdir -p ~/sqrock-internship/day8-usb-drop
cd ~/sqrock-internship/day8-usb-drop
```

Python was verified with:

```bash
python3 --version
```

The project script was created with:

```bash
nano usb_awareness.py
```

The script was then executed manually:

```bash
python3 usb_awareness.py
```

The resulting log was examined using:

```bash
cat recon_log.txt
```

---

## 📂 Project Structure

```text
day8-usb-drop/
│
├── usb_awareness.py
├── recon_log.txt
├── analysis.md
└── README.md
```

### File Description

| File               | Description                             |
| ------------------ | --------------------------------------- |
| `usb_awareness.py` | Benign USB security awareness script    |
| `recon_log.txt`    | Locally generated execution log         |
| `analysis.md`      | Security analysis and mitigation report |
| `README.md`        | Project documentation                   |

---

## 🛡️ USB Security Defenses

Organizations can reduce USB-related risks through multiple security controls.

### 1. Disable Automatic Execution

Systems should be configured to prevent automatic execution of programs from removable media.

### 2. User Awareness Training

Employees should be trained not to connect unknown USB devices to organizational computers.

### 3. Endpoint Protection

Endpoint security solutions can detect suspicious files and abnormal behavior.

### 4. Device Control

Organizations can restrict which USB devices are permitted on corporate systems.

### 5. Application Control

Only approved applications should be permitted to execute where appropriate.

### 6. Malware Scanning

Removable media should be scanned before files are opened or transferred.

### 7. Physical Security

Organizations should control access to USB devices and workstations.

---

## 🚨 USB Drop Attack Red Flags

Users should be cautious when they encounter:

* An unknown USB drive.
* A USB device found in a public location.
* A device labeled "Salary Information."
* A device labeled "Confidential."
* An unexpected USB device left near a workstation.
* Unknown executable files.
* Files requesting administrator privileges.
* Unexpected documents containing macros or scripts.

A suspicious USB device should **not** be connected to an organizational computer simply to determine its contents.

---

## 📈 Results

The simulation successfully demonstrated that a Python program can access basic information from the system on which it is executed.

The exercise showed that:

* A user should not automatically trust unknown USB devices.
* Executing unknown files can expose system information.
* Physical access can become an important security risk.
* Social engineering can be combined with removable media.
* Endpoint security and user awareness are important defensive layers.
* Simple system-information collection can demonstrate the potential impact of executing untrusted code.

---

## 🔐 Security and Ethical Considerations

This project was conducted strictly for **educational and authorized cybersecurity training**.

The following safeguards were maintained:

* The script was executed manually.
* No autorun functionality was implemented.
* No persistence mechanisms were created.
* No malicious software was developed.
* No credentials were collected.
* No private files were accessed.
* No external systems were targeted.
* No real users were affected.
* The exercise remained within the authorized laboratory environment.

> **Important:** Never execute unknown software or connect unknown USB devices to systems without proper authorization and security controls.

---


## 🎓 Learning Outcomes

After completing this project, I gained practical understanding of:

* USB drop attack concepts.
* Social engineering through physical media.
* Endpoint security risks.
* Python system-information modules.
* Local security logging.
* Linux file and directory operations.
* Security awareness principles.
* Defensive USB security controls.
* The importance of disabling automatic execution.
* Ethical cybersecurity testing.

---

## 📚 Key Security Concepts

```text
                 USB Drop Attack
                       │
                       ▼
              Physical Device
                       │
                       ▼
              Human Curiosity
                       │
                       ▼
              Device Connected
                       │
                       ▼
             File Potentially Opened
                       │
                       ▼
              Security Exposure
                       │
          ┌────────────┴────────────┐
          ▼                         ▼
    User Awareness            Endpoint Security
          │                         │
          ├── Training              ├── Device Control
          ├── Policies              ├── Malware Detection
          └── Reporting             └── Application Control
```

---

## 🏆 Project Conclusion

Day 8 provided practical exposure to **USB drop attacks, social engineering, endpoint security, and removable-media risks**.

By creating a benign Python awareness payload and executing it manually within a controlled Kali Linux laboratory, I was able to demonstrate how seemingly simple scripts can interact with the local system.

The project strengthened my understanding of **Python scripting, system information gathering, social engineering awareness, endpoint security, Linux operations, and ethical cybersecurity practices**.

---

# 👤 Author

Atemlefac Nkafu Bechem

Cybersecurity Engineer

LinkedIn: https://www.linkedin.com/in/atemlefac-nkafu-bechem-179987248

📌 Project Information Program Name: Cybersecurity internship at SQROCK | Week: 02 | Project 8: USB Drop Attack Simulation | Repository: GitHubing
