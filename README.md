# Hi, I'm Islam El-Badawy 👋

**DevSecOps / Cloud Engineer (junior)** · Cairo, Egypt

I build CI/CD pipelines that catch security problems **before** code reaches production, and I like finding the root cause when things break.
Communications & Computer Engineering graduate (2026) · CCNA · NTI DevSecOps program (D004).

---

## 🔐 Featured project: [SecureFlow](https://github.com/isl001/secureflow)

An end-to-end DevSecOps project for a FastAPI + PostgreSQL app: from a pull request to a running service on AWS.

**Pipeline.** Every pull request must pass **6 required checks** before it can merge:

| Gate | Tool | What it catches |
|---|---|---|
| `secret-scan` | Gitleaks (+ pre-commit hook) | passwords and tokens in the Git history |
| `sast` | SonarCloud Quality Gate | dangerous patterns in the code |
| `sca` | pip-audit (+ Dependabot, Snyk) | known CVEs in Python libraries |
| `image-scan` | Trivy | vulnerabilities inside the built Docker image |
| `dast` | OWASP ZAP | security issues in the **running** app |
| `build` | GitHub Actions + Docker | the app builds |

- Every gate was **proven with a negative test** (known-bad change → merge blocked).
- ZAP found a real bug: a NUL byte made the API crash with a 500 → fixed with input validation.
- Third-party actions pinned to commit SHAs, secrets kept out of Git, non-root multi-arch images on GHCR.
- A new base-image CVE (zlib) broke the image scan on an unrelated PR → verified, patched and documented.

**AWS.** The published image runs in a network I designed and built with the AWS CLI:

- 3-tier VPC across 2 Availability Zones (public / app / database subnets), one route table per tier, chained security groups → [design](https://github.com/isl001/secureflow/blob/main/docs/network.md)
- App server in a private subnet behind an Application Load Balancer: no public IP, no SSH (IAM role + Session Manager), IMDSv2 required
- Health-check failure tested on purpose, then everything that costs money cleaned up and verified → [deploy lab with screenshots](https://github.com/isl001/secureflow/blob/main/docs/deploy-aws-lab.md)

---

## 🧪 Other projects

- **[ElectroQA Studio](https://github.com/isl001/electroqa-studio)** — graduation project (5-person team). AI-assisted QA automation for Electron apps: an LLM agent explores the UI through Playwright MCP, generates Playwright tests, runs them and reports the results.
- **[Hotel Booking Cancellation Prediction](https://github.com/isl001/Hotel-Booking-Cancellation-Prediction)** — machine learning (EDA, feature engineering, Random Forest) deployed with Streamlit.
- **[Recipe App Android](https://github.com/isl001/Recipe-App-Android)** — Kotlin, MVVM, Room, Retrofit, offline favorites.

---

## 🛠️ Skills

**Hands-on:** Linux · Bash scripting · Git & GitHub Actions · Docker & Docker Compose · Python (automation) · Networking (CCNA: TCP/IP, DNS, HTTP, TLS)

**AWS:** IAM (users, policies, roles) · VPC (subnets, route tables, NAT, security groups, NACLs) · EC2 · ALB · Auto Scaling · RDS · S3 · Systems Manager Session Manager

**Security tools:** Gitleaks · SonarQube/SonarCloud · Snyk · pip-audit · Trivy · OWASP ZAP · Dependabot

**Currently working toward:** AWS Solutions Architect – Associate · Terraform · Kubernetes (CKA)

**Also:** AI & data science (Python, scikit-learn, Streamlit) · Android (Kotlin)

---

## 📫 Contact

[LinkedIn](https://www.linkedin.com/in/islam-hussein-44675a26a)
