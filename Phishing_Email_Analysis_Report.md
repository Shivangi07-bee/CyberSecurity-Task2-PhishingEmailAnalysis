#  Phishing Email Analysis Report

# 1. Email Sample (summary)
- Subject:** URGENT: Verify Your Account — Action Required  
- From (display): PayPal Support <support@paypal-secure.com>  
- Return-Path:bounce@malicious.ru  
- Received IP: 203.0.113.45  
- Attachment:invoice.zip  
- Link shown: https://www.paypal.com/verify  
- Actual link (href):** http://secure-paypall-login.ru/login?token=9f8b2c

# 2. Tools used
- Online header analyzer (e.g., MXToolbox / similar)
- Browser (hover link check)
- VirusTotal (for scanning suspicious links / attachments) — optional
- Local sandbox (if needed to inspect attachments) — **do not open untrusted attachments on your normal machine**

# 3. Indicators of Phishing (detailed)

| Indicator | Observation | Evidence |

Spoofed sender | Display shows PayPal, but domain is paypal-secure.com| From: support@paypal-secure.com |
Header discrepancies | Return-Path from malicious.ru, SPF fail | `Return-Path: <bounce@malicious.ru>`; Received-SPF: fail |
 Mismatched URLs | Link text claims `paypal.com` but href points elsewhere | `href="http://secure-paypall-login.ru/..."` |
Urgency / Threats | "verify ... within 24 hours" | Body text pressures immediate action |
 Suspicious attachment | `invoice.zip` attached | Unknown archive — common malware delivery |
 Security signatures absent | No DKIM, SPF fail | dkim=none; spf=fail` |

# 4. Conclusion
This email exhibits multiple, serious phishing indicators: mismatched sender domains, header/authentication failures, deceptive hyperlinks, urgent coercive language, and an unsolicited attachment. **Recommendation:** mark as phishing/spam, DO NOT click any links or open attachments, report to the security team, and block the sender domain.

# 5. Recommendations for users
1. Always hover over links to reveal the real URL before clicking.  
2. Check full email headers for SPF/DKIM results.  
3. Do not open attachments from unknown senders.  
4. When in doubt, access the service directly via your browser (type the official URL), not via email links.  
5. Report suspicious emails to your SOC or to the vendor (e.g., PayPal's phishing report address).

# 6. Appendix — Raw email (abbreviated)
*(Store a full .eml sample in this repo as phish_sample.eml for future reference and training.)*
