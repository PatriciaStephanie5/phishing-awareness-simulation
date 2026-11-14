# Recommendations

## 1. Employee Awareness (People Controls)

- Teach employees to inspect the actual sender address, urgency language, unexpected requests, and attachments before clicking.
- Demonstrate safe hyperlink inspection: hover or long-press to preview the real destination domain; never rely solely on the displayed link text.
- Publish a simple, low-friction reporting process (e.g., “Report Phish” button or dedicated mailbox) and make it visible in every inbox.
- Deliver short, role-specific follow-up training to groups that showed higher interaction rates (starting with HR and Marketing).
- Explicitly encourage staff to report accidental clicks immediately so the SOC can contain them quickly.

**Concrete example for hyperlink inspection**  
Display the difference between:
- Visible text: `https://mastercard-secure-login.com`  
- Actual destination: `https://mcrd-secure-login[.]xyz/login`  

## 2. Technical Controls

- Enforce SPF, DKIM and DMARC (at least `p=quarantine`, preferably `p=reject`) on all sending domains.
- Enable URL rewriting / time-of-click analysis and attachment sandboxing at the email gateway.
- Deploy endpoint protection with application control / allow-listing to reduce successful execution of malicious attachments.
- Require phishing-resistant MFA (FIDO2 / passkeys or hardware tokens) for privileged and high-risk accounts; standard MFA for all other accounts.
- Alert on anomalous sign-ins, impossible travel, and unusual mailbox or file-access behaviour.

## 3. Measurement & Continuous Improvement

Track the following metrics over successive campaigns:
- Reporting rate
- Repeat interaction rate (same user clicking in later simulations)
- Median time from click to report
- Training completion rate

Interpret results in context. Avoid punitive use of individual-level data; focus on organisational improvement.