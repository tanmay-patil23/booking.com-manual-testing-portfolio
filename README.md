# booking.com-manual-testing-portfolio
A lived-in set of real-world QA artefacts—traceability matrix, execution log, defect register, and sprint summary—capturing how a small tackled the Booking.com desktop site from every angle: payments, search, reviews, GDPR, accessibility, security, performance.
What’s inside
- rtm.csv
A pared-down Requirements Traceability Matrix that links user stories to explicit tests and, when things go sideways, to Jira tickets.

- test_execution_results.csv
Snapshot of an evening’s regression run: ten representative cases, pass/fail flags, defect hooks, build numbers—enough to prove we actually clicked the buttons.

- defect_log.csv
No sugar-coating. Three gnarly bugs, severity ratings, environments, open/close dates—the paper trail hiring managers always ask for.

- test-summary-report.md
A sprint-close narrative: scope, metrics, risks, recommendations. Think of it as the cliff-notes your PO skims before sign-off.

Why this matters
Manual tests still catch what scripts ignore: broken layouts on rotated tablets, multilingual profanity that slips past filters, last-minute SQL nasties. This repo shows the receipts—evidence of hands-on, eyes-on testing that protects revenue and reputation.

**Quick start**
Clone or fork the repo.

Pop the CSVs into your favourite spreadsheet tool.

Read the Markdown summary for context.

Lift anything you like into your own projects—credit appreciated, but not required.

**Stretch ideas**
Extend the RTM with mobile app user stories.

Convert high-value cases to Cypress or Playwright for CI.

Hook the defect log into your bug tracker via REST and track close-rates over time.

Happy hunting—and may your critical bugs surface in QA, not prod.
