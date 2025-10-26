### Header Analysis (MXToolbox)

From: "Amazon Support" <amazonsupport@amaz0n-payments.com>  
Return-Path: <mailer@randomdomain.xyz>  

SPF / DKIM / DMARC Results (as shown by MXToolbox):  
SPF Authenticated: ✖  
SPF Alignment: ✖  
DKIM Authenticated: ✖  
DMARC Compliant: ●

Received / Originating IP (from hop table):  
Received: from unknown 192.0.2.55

Interpretation:
- The From and Return-Path domains do not match → likely sender spoofing.
- SPF/DKIM are not authenticated → message not validated by sender domain mail servers (common with phishing).
- The originating IP (192.0.2.55) is not a known Amazon mail server → suspicious.

Evidence: see evidence/screenshots/header_analysis.png

--------------------------------------------------------------------------------------

Link Analysis
Displayed link text: https://www.amazon.com/secure

Actual link (target): http://amaz0n-secure-login.example.com/login

Observation:
The visible text pretends to be the official Amazon link (amazon.com), but the real destination is a fake domain (amaz0n-secure-login.example.com) which uses the number 0 instead of the letter o — a classic phishing trick.

VirusTotal Result:

Scanned URL: http://amaz0n-secure-login.example.com/login

Verdict: [Replace with your result → e.g., “No engines detected this URL as malicious (clean, example.com placeholder)” OR “Detected as Phishing by 5 security vendors.”]

Screenshot: evidence/virus_total/url1.png

Interpretation:

The mismatch between displayed and actual URLs shows an attempt to deceive users into clicking a fake login page.

Even though VirusTotal may show it as safe (since example.com is not a real malicious site), this pattern is typical of phishing emails that try to steal credentials.

The use of “amaz0n” (with a zero) instead of “amazon” is a typo-squatting method used by attackers to look legitimate.



---------------------------------------------------------------------------------
Social Engineering / Body Analysis

Email Greeting:

Dear Customer,


Urgent / Threatening Statement:

Your account will be permanently suspended in 24 hours unless you verify immediately.


Call-to-Action (Request):

Please verify here: https://www.amazon.com/secure


Language & Tone Observations:

The message uses urgency and fear (“permanently suspended in 24 hours”) to push the user into immediate action without thinking.

It includes a generic greeting (“Dear Customer”) instead of using the real name — a common phishing indicator.

The tone is official and threatening, typical of fake customer support messages impersonating big brands like Amazon.

The email asks the user to click a link and “verify” their account, a clear red flag.

Small spelling or style issues and a suspicious sender address further indicate that this is not a legitimate message.

Interpretation:
This message demonstrates the use of social engineering tactics — urgency, authority impersonation, and emotional pressure — to trick the recipient into clicking the malicious link and submitting login information.

Evidence:
See evidence/body.txt and screenshots folder (evidence/screenshots/inbox.png) for the full message content.



-----------------------------------------------------------------------------------------
Conclusion & Recommendations

Overall Conclusion:
The analyzed email is a phishing attempt that impersonates Amazon Support.
Multiple indicators confirm this:

Header mismatches: “From” and “Return-Path” domains differ.

SPF/DKIM failures: Sender authentication not verified.

Suspicious link: Mismatch between displayed and actual URL (uses “amaz0n” instead of “amazon”).

Social engineering: Urgent, fear-based language and fake verification request.

These patterns strongly indicate spoofing and credential-harvesting intent.

Recommended Actions:

Do not click any links or open attachments in the email.

Delete the email immediately from your inbox and spam folder.

Report it as phishing using your email client’s “Report phishing” option (e.g., Gmail → Report phishing).

If you already clicked or entered details, change your password immediately and enable two-factor authentication (2FA/MFA).

Educate other users about how to recognize such red flags.

Final Statement:
This investigation demonstrates how header analysis, URL inspection, and message content review can be combined to detect phishing.
All evidence (headers, link scan, screenshots) is included in the evidence/ folder and referenced throughout this report.