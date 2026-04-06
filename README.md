# AI-Assisted HID Recon Lab

## Overview
This project builds a lab-based system that combines a USB HID (Rubber Ducky–style) device with an AI-assisted analysis workflow. The goal is to simulate automated system reconnaissance in a controlled environment and use a large language model (LLM) to summarize security-relevant findings.

An Arduino Micro (ATmega32U4) is configured to emulate a USB keyboard. When plugged into a target machine (lab VM), it executes predefined reconnaissance scripts that collect system and network information. The collected data is saved to a USB flash drive and later analyzed using an AI prompt to produce structured security insights.

---

## Project Scope
- Environment: **Lab-only (virtual machines or personal test systems)**
- Target: Controlled systems owned by the project author
- Data: Non-sensitive, synthetic, or intentionally exposed system information
- Purpose: Demonstrate **automated data collection + AI-assisted security triage**

This project does **not** perform exploitation or target real-world systems.

---

## Objectives
- Automate system reconnaissance using a USB HID device
- Collect and store structured output from target systems
- Use AI to:
  - Summarize findings
  - Identify potential risks
  - Provide remediation suggestions
- Validate AI output against raw data for accuracy

---

## System Workflow
1. USB hub (with Arduino + flash drive) is plugged into the target machine
2. Arduino HID device executes a payload script
3. Reconnaissance commands run on the target system
4. Output is saved as a `.txt` report with device name and timestamp
5. Reports are stored on a USB flash drive labeled **DUCKY**
6. Reports are imported into an AI prompt for analysis
7. AI produces:
   - Summary
   - Key risks
   - Severity levels
   - Recommendations

---

## Tools & Technologies

### Hardware
- Arduino Micro (ATmega32U4)
- USB flash drive (labeled DUCKY)
- USB hub

### Software
- PowerShell / Bash (recon scripts)
- Nmap (network scanning)
- Arduino IDE (payload development)
- Large Language Model (LLM) for analysis

---

## Repository Structure
docs/
project-charter.md
methodology.md
prompt-template.md
findings/

scripts/
arduino/
recon_scripts/

README.md


---

## Methodology (High-Level)
- Develop HID payloads to execute reconnaissance commands
- Collect outputs into structured text files
- Store outputs using dynamic naming (device + timestamp)
- Analyze outputs using a standardized AI prompt
- Compare AI summaries with raw data to evaluate:
  - Accuracy
  - Missed findings
  - Incorrect interpretations

---

## AI Integration
AI is used as a **security analysis assistant**. A standardized prompt (see `docs/prompt-template.md`) is used to:

- Interpret raw system data
- Identify risks and vulnerabilities
- Provide evidence-based explanations
- Suggest mitigations

All AI outputs are validated against the original data.

---

## Ethics & Safety
- All testing is performed in a **controlled lab environment**
- No real systems, networks, or sensitive data are targeted
- Scripts are limited to **non-destructive reconnaissance**
- This project follows responsible cybersecurity practices

---

## Project Direction
This project falls under **Track A — AI for Security**, focusing on using AI to assist with security analysis and triage.

Future improvements may include:
- Automating the AI pipeline with an API
- Enhancing validation techniques
- Expanding dataset and test scenarios

---