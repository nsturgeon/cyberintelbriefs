# cyberintelbriefs
Curated Cyber Intelligence Reports

An automated cybersecurity intelligence pipeline built on Claude Code. Every morning it researches the day's security news and publishes a ranked briefing for defenders in Indianapolis and Indiana. From the briefing you can request a full intelligence report on any story and pick stories for a weekly summary.

What it produces
Daily briefing (7:00 AM ET). A single HTML page that opens with a Bottom Line Up Front, followed by:

News sorted by geography: Indianapolis, the State of Indiana, the United States, then global
Industry and market news: M&A, funding, product launches and leadership changes
A Patch & KEV watch table with the date each CVE was first published
Day-to-day changes in CISA's Known Exploited Vulnerabilities (KEV) catalog, diffed from daily snapshots
Also notable items and a sources footer
Every story carries severity, category and status badges, its original published and last update dates, and linked sources. Nothing older than five days is included. Indiana coverage includes FBI Indianapolis, both Indiana U.S. Attorney's Offices and regional outlets, as well as cyber-enabled crime such as fraud, BEC and sextortion cases.

Intelligence reports 
Each story on the briefing has a "Create intel report" button. A background worker researches the item in depth and writes a structured report with these sections:

Section	Contents
Bottom Line Up Front	Full summary, plus key judgments with estimative probability and confidence levels (ICD 203 style)
Indicators of Compromise	Every indicator stated in or derivable from the sources, defanged and labeled reported or derived
TTPs	MITRE ATT&CK mapping, threat actor profile and untested hunting queries (Sigma, KQL, SPL, Suricata)
Remediation Actions	Exposure table (CVSS, EPSS, KEV due date) and actions grouped as immediate, short term, long term and compensating, each with an owner
Sources	Every source used, graded on the Admiralty scale (A1–F6)
Miscellaneous	Timeline, local relevance, intelligence gaps and other notes
Each report has a report ID and version number. It also has a TLP 2.0 rating selector (CLEAR, GREEN, AMBER, AMBER+STRICT, RED, using CISA's definitions). The selector updates the banners and handling text, and it works both on the published page and in a local copy of the HTML file. Printing hides the selector box but keeps the TLP banners.
