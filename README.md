# Lab-VA
Social Engineering Exercises
# Phishing analysis
1. Overview
This investigation analyses a phishing-related email forwarded to the SOC for review. The objective of the analysis is to identify key artifacts such as the originating IP address, malicious URLs, hosting services, and webpage content by examining the email headers, attachments, and linked resources. Tools used include “Mozilla Thunderbird”, “URL2PNG” and “WHOIS”
2. Email Details
In the email, found details about sender and recipient

		Primary Recipient: kinnar1975@yahoo.co.uk 

		Subject: Undeliverable: Website contact form submission

		Date & Time Sent: 18 March 2021, 04:14

		Sender: Mailer-Daemon@se7-syd.hostedmail.net.au
3. Header Analysis
   3.1. Find the originating IP Address
   
   			The full email headers were examined using the “View Source” option in Thunderbird
   			IP Address Found : 103.9.171.10
   			IP represents the system that originally sent the phishing message
  	3.2. Reverse DNS Lookup

   			Reverse DNS Lookup of the originating IP to find the domain name indicates the message originated from a hosted server,
   			rather than a legitimate corporate mail server, which is a common indicator of phishing activity
   			Findings DNS Lookup : c5s2-1e-syd.hosting-services.net.au
   
4. Attachment Analysis
   	4.1. Attached File Name

   			The attached file name were give in a .eml file
   			Filename : Website contact form submission.eml

	 4.2. Malicious URL

   			phishing URL is present inside the email attachment
   			URL : https://35000usdperwwekpodf.blogspot.sg?p=9swghttps://35000usdperwwekpodf.blogspot.co.il?o=0hnd

5. Webpage and Hosting Analysis
   	5.1. Hosting Services

   			Malicious URL : “https://35000usdperwwekpodf.blogspot.sg?p=9swghttps://35000usdperwwekpodf.blogspot.co.il?o=0hnd”
   			The malicious URL attached in the email used a blogspot domain, indicating that the webpage is hosted on :Blogger.com
   			Free blogging platforms can be used by attackers to abuse. It is easy to set up and requires minimal identity verification
   
    5.2. URL2PNG to snap webpage

   			Submit the URL URL2PNG to capture a rendered snapshot of the webpage
   			confirms that the phishing page was previously active but has since been removed
   			The URL Redirect to Blogger website and show "Blog has been removed"
6. Conclusion

   		The email is confirmed to be part of a phishing campaign using fake website contact form submissions to distribute scam links. The attacker used a hosted server and free blogging platform to host malicious content,
   		attempting to lure victims with promises high daily earnings.
   		Although the phishing webpage has been taken down, the investigation successfully identified all relevant artifacts for threat intelligence and reporting.




