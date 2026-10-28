# SecureShop — Red Team & Application Security Assessment

## Build → Attack → Identify → Fix → Retest

SecureShop is a local e-commerce web application developed as part of a Red Team and Application Security assignment. The project demonstrates how to build a web application, identify security weaknesses using OWASP ZAP, investigate findings, implement remediation measures, and verify the effectiveness of security fixes.

## Project Overview

The application simulates an e-commerce platform with customer and administrator functionality. It is designed for controlled security testing in a local laboratory environment.

### Objectives

- Develop a functional e-commerce web application.
- Identify security weaknesses in application functionality and dependencies.
- Perform Dynamic Application Security Testing (DAST) using OWASP ZAP.
- Investigate and validate security findings.
- Map identified issues to relevant OWASP Top 10 categories.
- Implement security fixes and perform retesting.
- Document findings, remediation steps, and before-and-after results.

## Features

### Public Functionality
- Home page
- User registration and login
- Product listing and search
- Product details

### Authenticated Functionality
- User profile
- Shopping cart
- Order history

### Administrative Functionality
- Administrator login
- Product management
- User listing and management

## Technology Stack

The implementation may use the following technologies:

- **Backend:** Python with Flask
- **Frontend:** HTML5, CSS3, JavaScript
- **Database:** SQLite
- **Security Testing:** OWASP ZAP
- **Version Control:** Git and GitHub

*The technology stack should be updated to match the actual implementation.*

## Security Assessment Scope

The assignment requires at least four controlled security weaknesses from different categories. The assessment may cover:

| OWASP Category | Area of Investigation |
|---|---|
| A01: Broken Access Control | Authorization checks for protected resources |
| A03: Injection | Unsafe handling of user-supplied input |
| A05: Security Misconfiguration | Security headers and application configuration |
| A06: Vulnerable and Outdated Components | Dependency versions and security advisories |
| A07: Identification and Authentication Failures | Authentication and session management |
| A09: Security Logging and Monitoring Failures | Security event logging |

The final report must identify the weaknesses actually implemented and observed. These categories are assessment targets, not claims that every listed vulnerability has been confirmed.

## Project Workflow

1. **Build:** Develop the SecureShop application.
2. **Expose:** Run the application in an isolated local environment.
3. **Scan:** Configure OWASP ZAP and scan the authorized local target.
4. **Investigate:** Examine alerts, affected URLs, evidence, and potential impact.
5. **Validate:** Safely verify relevant findings within the lab.
6. **Fix:** Apply appropriate security remediations.
7. **Retest:** Repeat relevant tests and compare the results.
8. **Report:** Document the findings and security improvements.

## Installation and Setup

### Prerequisites

Install the following tools:

- Python 3
- pip
- Git
- OWASP ZAP

### Clone the Repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd SecureShop
```

Replace the placeholder with your actual repository URL.

### Create a Virtual Environment

Windows:

```bash
python -m venv venv
venv\Scripts\activate
```

Linux/macOS:

```bash
python3 -m venv venv
source venv/bin/activate
```

### Install Dependencies

If the repository contains a `requirements.txt` file:

```bash
pip install -r requirements.txt
```

### Run the Application

Use the entry point provided by the implementation. For example, if the application entry point is `app.py`:

```bash
python app.py
```

Open the local URL configured by the application, such as:

```text
http://127.0.0.1:5000
```

The port may differ depending on the actual configuration.

## OWASP ZAP Testing

1. Start SecureShop locally.
2. Open OWASP ZAP.
3. Set the target to your local application URL.
4. Crawl the application using an appropriate ZAP scanning mode.
5. Review the generated alerts.
6. Record severity, affected URLs, evidence, and recommended fixes.
7. Investigate relevant findings manually within the authorized lab.
8. Apply remediation and repeat the tests.

**Safety restriction:** Only scan the local application or another explicitly authorized lab target. Do not scan public websites, university systems, production applications, or systems belonging to others without explicit authorization.

## Vulnerability Investigation

For each significant finding, document:

- **What:** The identified vulnerability.
- **Where:** The affected URL, parameter, header, component, or feature.
- **Why:** The underlying cause.
- **Impact:** The potential security consequences.
- **Evidence:** The actual scanner output or safe validation result.
- **Remediation:** The code or configuration change applied.
- **Retest:** The result after remediation
