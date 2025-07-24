# Booking.com Manual Testing – Test Summary Report

## 1. Release Information
* **Application Under Test:** Booking.com consumer website (desktop)
* **Build:** v1.4.3 – EU-staging
* **Test Window:** 2025-07-24 – 2025-07-25
* **Team:** Manual QA Engineer (Tanmay Patil)

## 2. Scope Executed
The sprint covered 120 planned manual test cases drawn from critical functional, accessibility, privacy and security areas.  A representative subset (10 cases) is provided in `test_execution_results.xlsx` for demonstration purposes.  Full case catalogue available on request.

| Domain | Cases Executed | Pass | Fail | Blocked |
|--------|---------------:|-----:|-----:|--------:|
| Booking & Payments | 30 | 28 | 2 | 0 |
| Search & Filters | 18 | 18 | 0 | 0 |
| Reviews & Ratings | 10 | 9 | 1 | 0 |
| Account Management | 12 | 11 | 1 | 0 |
| Accessibility (WCAG) | 15 | 14 | 1 | 0 |
| GDPR Consent | 5 | 5 | 0 | 0 |
| Security (OWASP) | 20 | 17 | 3 | 0 |
| Performance Smoke | 10 | 10 | 0 | 0 |
| **Total** | **120** | **112** | **8** | **0** |

## 3. Defect Overview
Three high-impact defects were logged during execution (see `defect_log.xlsx`).

| Defect ID | Severity | Summary | Status |
|-----------|----------|---------|--------|
| DEF-1401 | Critical | Search API vulnerable to SQLi payload | Open |
| DEF-1148 | High | Layout breaks on orientation change | Open |
| DEF-1302 | Medium | Profanity filter fails on mixed language | In Progress |

## 4. Risk Assessment
* **Security Exposure:** Critical SQL injection vulnerability permits data exfiltration; release blocked until fixed.
* **Accessibility Debt:** Orientation defect fails WCAG 1.3.4; required for EU compliance.
* **Brand Reputation:** Review profanity could surface on production, harming trust.

## 5. Recommendations
1. Hot-fix DEF-1401 immediately; re-run full injection regression.
2. Patch responsive CSS for orientation; retest across iOS/Android.
3. Enhance machine-learning moderation to detect multilingual profanity variants.
4. Schedule targeted regression for affected modules after fixes.

## 6. Exit Criteria Evaluation
| Criterion | Target | Actual | Status |
|-----------|--------|--------|--------|
| Sev-1 defects | 0 | 1 | **Not Met** |
| WCAG AA Pass Rate | ≥ 95 % | 93 % | **Not Met** |
| Critical Path Pass | 100 % | 97 % | **Not Met** |

Release **rejected** pending resolution of critical items.

## 7. Attachments
* `rtm.xlsx` – Requirements Traceability Matrix
* `test_execution_results.xlsx` – Execution log
* `defect_log.xlsx` – Open defects register

---
*Report generated automatically on 2025-07-25.*