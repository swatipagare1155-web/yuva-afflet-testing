# Yuva Career Platform
## Affiliate Marketing, Referral Tracking, Commission Management & Payout Automation Platform

> **A secure, scalable, responsive, production-ready Affiliate Marketing and Referral Management System built for an educational organization selling online courses, training programs, and institutional certifications.**

---

### Core Highlights & Architectural Guarantees
- **Integer Paise Precision**: All calculations and ledger entries are stored and computed in integer paise (₹1.00 = 100 paise) — zero floating-point math.
- **Double-Entry Append-Only Ledger**: 37 normalized relational database tables tracking the complete lifecycle: Click $\rightarrow$ Lead $\rightarrow$ Order $\rightarrow$ Payment Verification $\rightarrow$ Commission Hold (15 days) $\rightarrow$ Payout Approval $\rightarrow$ Disbursal $\rightarrow$ Reconciliation.
- **Maker-Checker Payout Approval**: Finance Admin generates batches; secondary sign-off (Super Admin) is mandatory for batches exceeding ₹10,000.
- **Anti-Self-Approval & Anti-Fraud**: Strictly forbids affiliates or coordinators from approving their own payouts; automated self-referral and velocity detection.
- **Role-Based Access Control (RBAC)**: Least-privilege separation across Super Admin, Finance Admin, College Coordinator, Student Affiliate, and Auditor. Coordinators cannot view student bank details or passwords.
- **Section 194H TDS Compliance**: Automated statutory tax calculation (5% with PAN, 20% without PAN) and downloadable CSV ledger reports.
- **100% Automated Test Pass Rate**: 20/20 acceptance criteria scenarios verified.

---

### Quick Start Guide

#### 1. Setup & Installation
```bash
cd "H:\YUVA CAREER\yuva-platform"
npm install
```

#### 2. Seed Database
```bash
node database/seed.js
```

#### 3. Run Automated Acceptance Test Suite (20 Scenarios)
```bash
node tests/runAllTests.js
```

#### 4. Launch Application Server
```bash
node src/server.js
```
The server will be available at: **`http://localhost:3000`**

---

### Pre-Configured Demo Accounts (Password: `Password@123`)
| Role | Email | Key Permissions |
| :--- | :--- | :--- |
| **Super Admin** | `admin@yuvacareer.com` | Full governance, commission rules, approvals, audit logs |
| **Finance Admin** | `finance@yuvacareer.com` | Payout batches, maker approvals, reconciliation, TDS reports |
| **College Coordinator** | `coordinator@dtu.ac.in` | DTU student roster, team metrics, 2% coordinator override |
| **Student Affiliate** | `rahul.sharma@gmail.com` | Affiliate ID `YCC-AF-000001`, QR codes, ledger, payout profile |
| **Auditor** | `auditor@yuvacareer.com` | Read-only compliance, financial reconciliations, tax reports |

---

### Documentation Index
- [Architecture & Design Blueprint](../brain/system_architecture_and_design.md)
- [REST API Documentation](docs/API_DOCUMENTATION.md)
- [Commission Calculation Engine](docs/COMMISSION_CALCULATION_DOC.md)
- [Payout & Reconciliation SOP](docs/PAYOUT_AND_RECONCILIATION_SOP.md)
- [Super Admin User Manual](docs/ADMIN_USER_MANUAL.md)
- [Affiliate User Manual](docs/AFFILIATE_USER_MANUAL.md)
- [Privacy Policy & Affiliate Agreement Template](docs/PRIVACY_POLICY_AND_TERMS.md)
- [Production Security Checklist](docs/SECURITY_CHECKLIST.md)
- [Deployment & Disaster Recovery Guide](docs/DEPLOYMENT_AND_BACKUP_GUIDE.md)
