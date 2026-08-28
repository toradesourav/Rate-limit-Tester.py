# Rate-limit-Tester.py
🛡️ Checks if OTP/login endpoints block after limited failed attempts | Detects CWE-307 Missing Rate Limiting | SOC &amp; Bug Bounty Lab #46
# Rate Limit Tester

Checks if OTP/login endpoint has proper rate limiting.

### How it works
- Sends only 10 fake requests
- Checks for 429 / 403 status
- If no block after 10 attempts = Vulnerable

### Finding Type
CWE-307: Improper Restriction of Excessive Authentication Attempts

### Fix
Implement 429 + lockout after 5 failed attempts.
