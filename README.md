# Hi, I'm Islam Hussein 👋

**Junior DevSecOps / Cloud Engineer** · Cairo, Egypt

I build CI/CD pipelines that catch security problems **before** code reaches production, and I like finding the root cause when things break.
Communications & Computer Engineering graduate (2026) · CCNA · NTI DevSecOps program (D004).

---

## 🔐 Featured project: [SecureFlow](https://github.com/isl001/secureflow)

An end-to-end DevSecOps pipeline for a FastAPI + PostgreSQL app. Every pull request must pass **6 required checks** before it can merge:

| Gate | Tool | What it catches |
|---|---|---|
| `secret-scan` | Gitleaks (+ pre-commit hook) | passwords and tokens in the Git history |
| `sast` | SonarCloud Quality Gate | dangerous patterns in the code |
| `sca` | pip-audit (+ Dependabot, Snyk) | known CVEs in Python libraries |
| `image-scan` | Trivy | vulnerabilities inside the built Docker image |
| `dast` | OWASP ZAP | security issues in the **running** app |
| `build` | GitHub Actions + Docker | the app builds |

Highlights:
- Every gate was **tested with a negative test** (known-bad code → merge blocked).
- ZAP found a real bug: a NUL byte made the API crash with a 500 → fixed with input validation.
- Third-party actions pinned to commit SHAs, secrets kept out of Git, non-root multi-arch images on GHCR.
- Triage decisions (fix / accept / false positive) documented in the README.

---

## 🧪 Other projects

- **[ElectroQA Studio](https://github.com/isl001/electroqa-studio)** — graduation project (5-person team). AI-assisted QA automation for Electron apps: an LLM agent explores the UI through Playwright MCP, generates Playwright tests, runs them and reports the results.
- **[Hotel Booking Cancellation Prediction](https://github.com/isl001/Hotel-Booking-Cancellation-Prediction)** — machine learning (EDA, feature engineering, Random Forest) deployed with Streamlit.
- **[Recipe App Android](https://github.com/isl001/Recipe-App-Android)** — Kotlin, MVVM, Room, Retrofit, offline favorites.

---

## 🛠️ Skills

**Hands-on:** Linux · Bash · Python · Git & GitHub Actions · Docker & Docker Compose · AWS (IAM, EC2, ALB, Auto Scaling, RDS, S3, CloudWatch) · Networking (CCNA: TCP/IP, DNS, HTTP, TLS)

**Security tools:** Gitleaks · SonarQube/SonarCloud · Snyk · pip-audit · Trivy · OWASP ZAP · Dependabot

**Currently learning:** Kubernetes · Terraform · Ansible · Prometheus & Grafana · Jenkins

**Also:** AI & data science (Python, scikit-learn, Streamlit) · Android (Kotlin)

---

## 📫 Contact

[LinkedIn](https://www.linkedin.com/in/islam-hussein-44675a26a)
