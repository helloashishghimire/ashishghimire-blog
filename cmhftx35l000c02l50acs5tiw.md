---
title: "🌐 Unusual Network Volume? Here’s How I Tracked It Down!"
datePublished: Sat Nov 01 2025 05:15:55 GMT+0000 (Coordinated Universal Time)
cuid: cmhftx35l000c02l50acs5tiw
slug: unusual-network-volume-heres-how-i-tracked-it-down
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1761974146811/0f44e275-cdb9-48c7-a482-82995426ece8.jpeg

---

The other day, I spotted a sudden spike in outbound traffic on our Splunk dashboards. At first glance, it looked like possible data exfiltration — unusual volumes going out always raise alarms.  
Here’s how I broke it down:

Top talkers & destinations → Identified which IPs and ports were responsible for the surge  
Traffic volume → Looked at session counts, transfer rates, and total bytes  
Reputation checks → Enriched with AbuseIPDB, VirusTotal, and WHOIS to verify the external IPs  
Context → Cross-checked Azure AD sign-ins, MFA status, and endpoint activity for anomalies  
After correlating the data, the finding was clear: the spike was legitimate DNS traffic heading to Cisco DNS servers, not an attack.  
👉 Lesson learned: Big traffic spikes don’t always mean compromise. Combining dashboards, enrichment, and context quickly separates normal infrastructure traffic from real threats.  
[**hashtag#dayinlifeofSOCAnalyst**](https://www.linkedin.com/search/results/all/?keywords=%23dayinlifeofsocanalyst&origin=HASH_TAG_FROM_FEED) [**hashtag#SIEM**](https://www.linkedin.com/search/results/all/?keywords=%23siem&origin=HASH_TAG_FROM_FEED) [**hashtag#SOC**](https://www.linkedin.com/search/results/all/?keywords=%23soc&origin=HASH_TAG_FROM_FEED) [**hashtag#Threathunting**](https://www.linkedin.com/search/results/all/?keywords=%23threathunting&origin=HASH_TAG_FROM_FEED)