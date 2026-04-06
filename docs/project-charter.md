# Project Charter
## AI-Assisted HID Recon Lab

---

## 1. Scope & Rules of Engagement (ROE)

This project is conducted strictly in a **controlled lab environment**.

### Authorized Targets:
- Personal virtual machines (e.g., Kali Linux, Windows VM)
- Local test systems owned by the project author

### Unauthorized Targets:
- Any external systems or networks
- Devices without explicit ownership and permission
- Real-world production environments

### Data Constraints:
- Only non-sensitive, synthetic, or lab-generated data will be used
- No credentials, personal data, or confidential information will be collected

---

## 2. Project Objective

The objective of this project is to design and evaluate a system that:

- Uses a USB HID device (Arduino-based) to automate system reconnaissance
- Collects system and network information from a target machine
- Stores collected data in structured report files
- Applies an AI model to summarize findings and identify potential risks
- Evaluates the accuracy and usefulness of AI-generated security insights

---

## 3. Methodology

The project will follow a three-phase workflow:

### Phase 1: Data Collection
- Develop Arduino HID payloads to execute reconnaissance commands
- Run scripts on the target system (e.g., system info, network configuration, port scanning)
- Save outputs as `.txt` reports labeled with device name and timestamp
- Store reports on a USB flash drive labeled "DUCKY"

### Phase 2: Data Analysis
- Import collected reports into the analysis environment
- Use a standardized AI prompt to analyze raw output
- Generate:
  - System summary
  - Identified risks
  - Severity classification
  - Recommended mitigations

### Phase 3: Validation
- Compare AI-generated summaries against raw data
- Identify:
  - Missed findings
  - Incorrect interpretations
  - Improvements after prompt refinement

---

## 4. Tools & Technologies

### Hardware
- Arduino Micro (ATmega32U4)
- USB flash drive (DUCKY)
- USB hub

### Software
- Arduino IDE
- PowerShell / Bash scripting
- Nmap (network scanning)
- Large Language Model (LLM) for analysis

---

## 5. Milestones (Weeks 2–4)

### Week 2
- Complete Arduino HID payload development
- Implement basic reconnaissance scripts
- Successfully generate and store report files

### Week 3
- Develop AI prompt and analysis workflow
- Perform multiple test runs
- Begin collecting dataset of reports

### Week 4
- Evaluate AI output vs raw data
- Refine prompts for improved accuracy
- Prepare final report and presentation materials

---

## 6. Success Criteria

The project will be considered successful if:

- The HID device reliably executes reconnaissance scripts
- Reports are generated and stored with correct naming format
- AI produces structured summaries from raw data
- AI findings can be validated against original outputs
- Improvements in AI accuracy are demonstrated through prompt tuning

---

## 7. Ethics & Safety Statement

This project adheres to ethical cybersecurity practices:

- All activities are conducted in a **lab-only environment**
- No real systems or unauthorized networks are targeted
- Scripts are limited to **non-destructive reconnaissance**
- No exploitation, persistence, or data exfiltration is performed
- The project is intended for educational purposes only

---

## 8. Risks & Limitations

- AI may produce inaccurate or incomplete summaries (hallucination risk)
- HID timing issues may affect script execution reliability
- Variability in system configurations may affect results

Mitigation:
- Validate all AI outputs against raw data
- Use structured prompts to reduce ambiguity
- Perform repeated testing across multiple runs

---