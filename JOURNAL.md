# Week 7 — Issue selection

## Issue selection notes

- The issue is scoped to a single file (`safety/pii_scrubber.py`).
- The estimated effort is small enough for this module.
- The bug has a clear expected behavior: email addresses should be redacted.
- I can test the fix by checking that generated feedback no longer contains email addresses.

**Issue link:** https://github.com/jamjamgobambam/pathreview/issues/61

**Issue title:** PII scrubber doesn't redact email addresses in generated feedback

**Tier:** [x] Tier 1  [ ] Tier 2  [ ] Tier 3

**Problem summary:**
This issue affects the PII scrubbing safety layer in the backend. The email detection regex was removed during a refactor, causing email addresses extracted from resumes to appear unchanged in generated feedback. A successful fix should restore email address detection and ensure generated feedback removes this type of personally identifiable information before being shown to users.

**Branch name:** fix/61-pii-email-redaction

**Setup confirmation:** [x] App runs locally at localhost/5173

**Cohort ledger:** [ ] Issue added to cohort ledger
