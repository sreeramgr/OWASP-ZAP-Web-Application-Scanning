# Web Application Scanning with OWASP ZAP

## Project Overview

This project demonstrates web application vulnerability scanning using OWASP ZAP against OWASP Juice Shop, an intentionally vulnerable web application hosted locally using Docker.

The goal of this project was to identify common web application security issues, analyze ZAP alerts, understand their risk levels, and document practical remediation steps.

## Objective

The objective of this project was to gain hands-on experience with web application vulnerability assessment by:

- Setting up a local vulnerable web application
- Capturing and analyzing web traffic using OWASP ZAP
- Running automated scanning and AJAX Spider
- Reviewing security alerts
- Documenting findings, impact, and remediation steps

## Lab Scope

Target application:

```text
http://localhost:3000
```

The assessment was performed only against the locally hosted OWASP Juice Shop application. No public, university, company, or third-party websites were intentionally scanned.

## Tools Used

- OWASP ZAP
- OWASP Juice Shop
- Docker Desktop
- Java 17
- Windows Command Prompt
- Browser launched through OWASP ZAP

## Lab Setup

OWASP Juice Shop was deployed locally using Docker and accessed through the browser at:

```text
http://localhost:3000
```

OWASP ZAP was used to inspect application traffic, crawl the application, run AJAX Spider, and review the generated security alerts.

## Methodology

1. Installed Java 17, Docker Desktop, and OWASP ZAP.
2. Deployed OWASP Juice Shop locally using Docker.
3. Verified that the application was accessible at `http://localhost:3000`.
4. Opened OWASP ZAP and configured the local target.
5. Performed automated scanning using OWASP ZAP.
6. Used manual browsing to capture application traffic.
7. Used AJAX Spider to improve scan coverage for the JavaScript-heavy application.
8. Reviewed ZAP alerts based on risk level, confidence, evidence, and recommended solution.
9. Captured screenshots of key findings.
10. Generated an OWASP ZAP HTML report.
11. Documented findings, impact, and remediation steps.

## Key Findings

| No. | Finding | Risk | Category |
|---|---|---|---|
| 1 | Content Security Policy Header Not Set | Medium | Security Misconfiguration |
| 2 | Cross-Domain Misconfiguration | Medium | Broken Access Control |
| 3 | Missing Anti-clickjacking Header | Medium | Security Misconfiguration |
| 4 | Session ID in URL Rewrite | Medium | Session Management |
| 5 | Private IP Disclosure | Low | Information Disclosure |
| 6 | Timestamp Disclosure - Unix | Low | Information Disclosure |
| 7 | X-Content-Type-Options Header Missing | Low | Security Misconfiguration |
| 8 | Information in Browser sessionStorage | Informational | Client-Side Storage Observation |
| 9 | Modern Web Application | Informational | Scan Coverage Observation |

## Findings Summary

The scan identified multiple web application security issues, mainly related to missing security headers, permissive CORS configuration, session identifier exposure, and information disclosure.

The most important findings were:

- Missing Content Security Policy header, which can weaken browser-side protection against script injection attacks.
- Permissive CORS configuration using wildcard origin access.
- Missing anti-clickjacking protection on some responses.
- Session identifier exposure through URL parameters.
- Disclosure of private IP and timestamp information.
- Missing `X-Content-Type-Options: nosniff` header on some responses.

## Project Files

- [Vulnerability Assessment Summary](docs/vulnerability-assessment-summary.md)
- [Commands Used](commands-used.md)
- [ZAP HTML Report](reports/zap-scan-report-localhost-only.html)
- [Screenshots](screenshots/)

## Skills Demonstrated

- Web application vulnerability scanning
- OWASP ZAP usage
- Docker-based lab setup
- Security alert analysis
- HTTP response header review
- Vulnerability documentation
- Remediation planning
- GitHub project documentation

## Outcome

This project helped me understand how web application scanning is performed using OWASP ZAP. I learned how to set up a vulnerable application in a local lab, scan it safely, analyze security findings, and document remediation steps in a structured format.

## Disclaimer

This project was completed in a local lab environment using OWASP Juice Shop. Testing was performed only against systems owned and controlled in the lab environment. This project is intended for educational and portfolio purposes only.
