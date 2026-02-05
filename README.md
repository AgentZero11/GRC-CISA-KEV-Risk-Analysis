# GRC-CISA-KEV-Risk-Analysis
## Executive Summary
Traditional vulnerability management often relies solely on CVSS scores, which measure theoretical severity rather than actual threat activity. This project analyzes the CISA Known Exploited Vulnerabilities (KEV) catalog against the CVE Master dataset to identify the Root Cause Weaknesses (CWEs) that attackers are most successfully weaponizing.

By joining threat intelligence with technical descriptions, this analysis identifies systemic security gaps and maps them to NIST 800-53 and ISO 27001 controls to drive data-driven governance and remediation strategies.

## Technical Stack
* Language: Python 3.x
* Data Analysis: Pandas, NumPy
* Database: SQL (SQLite) for cross-dataset joins
* Visualization: Matplotlib, Seaborn
* Frameworks: NIST 800-53 Rev. 5, ISO 27001:2022

## Key Findings
Through the correlation of CISA threat data and CWE root causes, the following insights were identified:
* Input Validation Failures: Over 40% of the top 10 exploited vulnerabilities share a common root cause in improper input handling (CWE-20, 79, 89, 77).
* Memory Safety: Memory corruption issues (CWE-787) remain the #1 driver for Remote Code Execution (RCE) in legacy platforms.
* Control Concentration: Focusing remediation efforts on NIST SI-10 (Information Input Validation) provides the highest "Return on Security Investment" (RoSI) for the current threat landscape.

## Project Structure
* [CWE_Root_Cause_Analysis.ipynb](https://github.com/AgentZero11/GRC-CISA-KEV-Risk-Analysis/blob/main/GRC_Strategy(CWE_Analysis).ipynb): The primary Python notebook containing the ETL pipeline and SQL analysis.
* [Enterprise_Secure_Software_Policy.md](https://github.com/AgentZero11/GRC-CISA-KEV-Risk-Analysis/blob/main/Enterprise_Secure_Software_Policy.md): A formal GRC policy drafted based on the data findings, mapping CWEs to regulatory controls.
* [CISO_Summary.md](https://github.com/AgentZero11/GRC-CISA-KEV-Risk-Analysis/blob/main/CISO_Summary.md): An executive-level briefing translated for non-technical leadership.
* [requirements.txt](https://github.com/AgentZero11/GRC-CISA-KEV-Risk-Analysis/blob/main/requirements.txt): List of dependencies required to reproduce the environment.

## How to Run
* Clone the Repository:

```
  git clone https://github.com/AgentZero11/GRC-CISA-KEV-Risk-Analysis.git

  cd GRC-CISA-KEV-Risk-Analysis
```

* Install Dependencies:

```
  pip install -r requirements.txt
```
  
* Execute the Analysis: Open the ```.ipynb``` file in Jupyter Lab or VS Code and run all cells to regenerate the database joins and visualizations.

## Author
Jah Tyler
* **Role:** Aspiring Security Data / GRC Analyst

* **LinkedIn:** [Jah Tyler](https://www.linkedin.com/in/jah-tyler-153802107/)

* **GitHub:**  @AgentZero11
