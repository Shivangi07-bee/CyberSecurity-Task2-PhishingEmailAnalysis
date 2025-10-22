# Task 2 — Phishing Email Analysis

#  Objective
The main aim of this task was to identify and analyze phishing characteristics in a suspicious email sample.  
By doing this, I learned how to check for fake sender addresses, header mismatches, malicious links, attachments, and social engineering tricks used by attackers.


#What I Did

1. Collected a phishing email sample**  
   I used a safe sample email that mimicked a PayPal alert asking to “verify account”.  
   It contained fake links and a suspicious attachment named `invoice.zip`.

2. Checked sender details and headers**  
   I copied the full email header and analyzed it using the online tool [MXToolbox Email Header Analyzer](https://mxtoolbox.com/EmailHeaders.aspx).  
   The results showed SPF failure, missing DKIM, and mismatched return-paths — all signs of a spoofed sender.

3. Inspected links and attachments**  
   The displayed link looked like `https://www.paypal.com/verify` but when hovered, it redirected to  
   `http://secure-paypall-login.ru/login`.  
   The `.zip` attachment was also suspicious, so it was treated as malicious and not opened.

4. Checked the language of the email**  
   The content used urgent words like *“verify immediately”* and *“within 24 hours”*, which is a typical pressure tactic used in phishing attacks.

5. Created a summary report**  
   I made a detailed Markdown report named **Phishing_Email_Analysis_Report.md**, listing all phishing indicators, screenshots, and a short conclusion.

# Files in This Repository

| File Name | Description |
Phishing_Email_Analysis_Report.md` - Main analysis report containing all phishing indicators and evidence |
phish_sample.eml` -  Raw phishing email sample used for analysis |
screenshots/ - Folder containing screenshots of the email header and analyzer results |
README.md` - This file, explaining the overall task process |

#  Tools and Resources Used
- **MXToolbox Header Analyzer** – for header and SPF/DKIM checks  
- **PhishTank** – to review phishing examples  
- **VirusTotal (optional)** – to scan suspicious links or attachments  
- **VS Code / Notepad++** – for viewing `.eml` text  
- **GitHub** – for report submission and version control

#  Observations

- Sender domain was not official (`paypal-secure.com` instead of `paypal.com`)
- SPF failed and DKIM was missing
- Hyperlink text didn’t match the real destination
- Contained urgency and a time limit (social engineering trick)
- Attached a zip file with unknown content

#  Conclusion

The analyzed email clearly showed multiple phishing indicators:
- **Spoofed sender**
- **Header discrepancies**
- **Mismatched URLs**
- **Urgent/Threatening tone**
- **Malicious attachment**

Such emails should be reported and never interacted with.  
This task helped me understand real-world phishing techniques and how to recognize them quickly during security assessments.


# Author
Name: Shivangi Chauhan 
Course: B.Tech CSE (Cybersecurity Specialization)  
Task: 2 — Phishing Email Analysis  
Date: 22 Oct 2025
