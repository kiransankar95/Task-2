# Task-2
Identifying phishing characteristics in a suspicious email sample.



Downloaded a sample phishing email (.eml file) from an Opensource GitHub repository.

Opened the email using Thunderbird on Kali Linux.

Copied the email header from Thunderbird.

Analyzed the header using MXToolbox Header Analyzer.



🔎HEADER ANALYSIS:
Field	Details
From	Microsoft account team no-reply@access-accsecurity.com
Reply-To	sotrecognizd@gmail.com
Return Path	bounce@thcultarfdes.co.uk     
Sender IP	89.144.44.2
SPF	None — Domain did not authorize this sender
DKIM/DMARC	Not configured
Subject	Microsoft account unusual signin activity
Date	Fri, 8 Sep 2023 05:47:04 +0000




🔍HEADER FINDINGS:
Sender domain mismatch: The "From" address claims to be Microsoft but uses a suspicious domain (access-accsecurity.com).
Return Path and Reply-To: Both use unrelated domains (thcultarfdes.co.uk, gmail.com), indicating likely spoofing.
SPF Failure & DMARC Not Configured: The email lacks proper authentication, a common phishing trait.
High Priority Flag: Set to invoke urgency.





🎣PHISHING INDICATORS IDENTIFIED:
Indicator Type	Description
Spoofed Email Address	Appears to be Microsoft, but the domain is fake (access-accsecurity.com).
Fake Reply Address	Replies are sent to a Gmail account (sotrecognizd@gmail.com).
Suspicious Links	The “Report the User” button is a mailto: link to sotrecognizd@gmail.com, not Microsoft.
Threatening/Urgent Language	Uses urgent language: “If this wasn't you, please report the user"
Mismatch in Message & Links	Appears to be a login alert, but links open an email composer instead of a Microsoft page.
Grammar Errors	Phrases like "sign.in activity", inconsistent spacing/punctuation.
Unfamiliar IP/Location	Claims a login from “Russia/Moscow” using 103.225.77.255 to induce fear.
No Official Branding	No digital signature, official footer, or policy links.




CONCLUSION:
This email contains multiple classic phishing indicators, including:

Spoofed sender and reply addresses
Urgent and manipulative language
Suspicious links and tracking pixels
Authentication failures (SPF/DKIM/DMARC)
Grammar errors, and lack of branding
