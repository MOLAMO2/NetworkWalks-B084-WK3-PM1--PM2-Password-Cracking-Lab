<p align="center">
  <img src="assets/header.svg" alt="NetworkWalks Cybersecurity Training — Password Cracking & PDF Forensics banner" width="100%">
</p>

# NetworkWalks-B084-WK3-PM1-PM2-Password-Cracking-Lab

## Week 3 — Password Cracking Lab

**John the Ripper · Johnny GUI · Networkwalks tools · Kali Linux**

A clear record of the Week 3 cybersecurity lab activities: extracting password hashes, running dictionary attacks in an authorised lab environment, and documenting the results with screenshots.

> **Lab use only:** Perform password-recovery tests only on files and systems you own or have explicit permission to assess.

## Contents

- [Project overview](#project-overview)
- [Repository structure](#repository-structure)
- [Module 1 -John the Ripper and Johnny](#module-1--john-the-ripper-and-johnny)
- [Module 2 -Networkwalks browser tools](#module-2--networkwalks-browser-tools)
- [Bonus - Kali Linux](#bonus--kali-linux)
- [Key lessons](#key-lessons)
- [Tools and references](#tools-and-references)

## Project overview

A password-protected document or archive can contain a verifier in the form of a **password hash**. In this lab, a hash is extracted from the authorised test file and supplied to a password-auditing tool. The tool tests candidate passwords until it finds a match.

The work is organised into three parts:

1. **Module 1:** Use John the Ripper (JTR) and its Johnny graphical interface on Windows.
2. **Module 2:** Use the Networkwalks Hash Calculator and Password Cracker in a browser.
3. **Bonus:** Use `pdf2john`, `zip2john`, John the Ripper and the `rockyou` wordlist on Kali Linux.

## Repository structure

```text
NetworkWalks-B084-WK3-PM1-PM2-Password-Cracking-Lab/
├── README.md
├── assets/
│   └── header.svg
├── hashes/
│   ├── hash1.txt
│   ├── hash2.txt
│   ├── hash3.txt
│   ├── locked1_pdf.txt
│   └── pdf1_hash.txt
└── screenshots/
    ├── 01_hash_calculator_pdf1.png
    ├── 02_password_cracker_success.png
    ├── 03_johnny_settings_john_exe.png
    ├── 04_johnny_cracked_good-luck.png
    ├── 05_pdf1_opened_flag.png
    └── 06_kali_john_rockyou.png
```

**Folders**

- `assets/` — project banner.
- `hashes/` — hash files and captured cracking output from the lab.
- `screenshots/` — visual evidence of the steps and results.

## Module 1 — John the Ripper and Johnny

**Task:** Recover the password for the lab PDF (`My Locked PDF1.pdf`) using John the Ripper and Johnny on Windows.

### Steps performed

1. Downloaded the Jumbo version of John the Ripper and the Johnny GUI.
2. Opened Johnny settings and selected `john.exe` from the John installation's `run` folder.
3. Confirmed that Johnny detected John the Ripper.
4. Loaded the file containing the extracted PDF hash.
5. Started the password audit and checked the **Passwords** tab for the result.

### Result

| Item | Result |
|---|---|
| Target | `My Locked PDF1.pdf` |
| Hash type | PDF (`$pdf$` format) |
| Tool | Johnny / John the Ripper 1.9.0-jumbo-1 |
| Status | 1 hash recovered; 0 remaining |
| Lab result | `good-luck` |

The recovered lab password opened the PDF and displayed the captured flag page.
