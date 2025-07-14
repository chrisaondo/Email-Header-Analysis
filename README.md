<h1>Email Header Analysis</h1>


<h2>Description</h2>
This project documents the forensic analysis of a spoofed phishing email impersonating Apple ID Support. The goal was to dissect both the email headers and body to uncover signs of spoofing, credential phishing, and malware delivery.  skills crucial for a SOC Analyst or Email Security Investigator role.
<br />


<h2>Project Overview</h2>

- <b>Target: VIP user at executive-target.com</b> 
- <b>Email Source: Spoofed domain appleid-verification.com</b>
- <b>Main Threats:</b>
  - <b>Social engineering via urgency in subject line.</b>
  - <b>Credential phishing via fake verification link.</b>
  - <b>Malware delivery through .exe attachment disguised as a PDF.</b>
<h2>Techniques Used</h2>

- <b>Header analysis (SPF, DKIM, DMARC)</b>
- <b>IP and domain verification (RFC5737 reserved block detection)</b>
- <b>MIME and attachment inspection</b>
- <b>Phishing link inspection</b>
- <b>VirusTotal detection simulation</b>
<h2> Key Findings</h2>

| Indicator                                               | Verdict                               |
|:---------------------------------------------------------|:---------------------------------------|
| DKIM & DMARC                                            | Fail – Spoofed domain                 |
| SPF	|Pass, but on a malicious lookalike domain                                                 |
| IP Address	|198.51.100.77 – Reserved block, not routable                                        |
| Subject Line                                            | Urgent CTA – Classic phishing trigger |
| Body                                                    | HTML with fake verification link      |
| Attachment                                              | .pdf.exe – Likely malware             |
| VirusTotal Result                                       | 8/65 AV detections                    |


<h2>Forensic Artifacts & Screenshots

</h2>
<p align="left">
Analyzing SPF, DKIM, and DMARC authentication results. <br/>
<br/>
<img src="https://github.com/chrisaondo/Email-Header-Analysis/blob/main/Authentication_Failed.png"/>
<br />
<br />
IP address used in spoofed email is non-routable (RFC5737).  <br/>
<img src="https://github.com/chrisaondo/Email-Header-Analysis/blob/main/Reserved_IP.png"/>
<br />
<br />
Malicious attachment using double extension to deceive users. <br/>
<img src="https://github.com/chrisaondo/Email-Header-Analysis/blob/main/Double_Attachment.png"/>
<br />
<br />
Malware payload detected by multiple AV engines on VirusTotal.  <br/>
<img src="https://github.com/chrisaondo/Email-Header-Analysis/blob/main/Virus_total.png"/>
<br />
<br />

The subject line uses urgency-based social engineering, a hallmark of phishing campaigns, intended to pressure the recipient into immediate, uncritical action.<br/>
<img src="https://github.com/chrisaondo/Email-Header-Analysis/blob/main/Subject.png"/>
<br />
<br />
<h2>Skills Demonstrated</h2>

- <b>Email forensics & threat detection</b>
- <b>Security protocol interpretation (SPF/DKIM/DMARC)</b>
- <b>Malware artifact identification</b>
- <b>Social engineering analysis</b>
- <b>Communication of technical findings to non-technical audiences</b>
<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
