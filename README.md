---
title: 'Golkonda'
date: 2023-02-27
excerpt: 'Egress control and Mitre Att&ck dashboard'
author: ['David Arthur']
coverImage: ''
tags: ['Hackfest', 'ANZ, Japan, ASEAN', 'Big-IP, Telemetry Streaming, iRules, ILX, Elastic Search, Kibana, Log Stash, Virus Total']
team: ['Yukio Ito', 'James Lee', 'Kayvan Farzaneh', 'Cameron Jenkins']
sponsor: []
mentor: ['David Arthur']
---
## Project Description

Solution to help Blue Teams struggling with egress control and identifying malicious activities like C&C (C2) and data exfiltration

## Key Hypothesis

Using the Big-IP full proxy architecture and security modules, it is possible to configure a difficult to bypass, if not impregnable, egress control point from customer environments. Additionally, by understanding Mitre Att&ck techniques to acheive the Command and Control (C&C) and Exfiltration (exfil) tactics, that customer alerts can be generated to give Blue teams high fidelity signals of malicious activity and / or compromised end points.

## How It Works

The solution comprises a Big-IP system(s) with custom configurations for handling common C&C and exfil techniques; e.g.: DNS, HTTP, HTTPS, NTP, ICMP, etc. Profiles, iRules, etc. are then configured to look for specific indicators of Att&ck techniques and generate customer logging, along with the Mitre Att&ck technique and / or Tactic nomenclature, to an extenal ELK system for visualtisation. Additionally, an iRules LX (ILX) module has been written to do a sideband call out to Virus Total (VT) for additional validation and enrichment; this could be expanded to support other external threat intel systems. 

Once sent to the ELK platform, a custom dashboard has been created to surface the alert(s), the Mitre technique and / or tactic identifier, link to relevant Mitre Att&ck page, details on end-point, C&C and / or exfil destination, VT enrichment, etc.

The intent is for this to be able to be configured in three mains ways; visibility only (i.e.: alerting but no blockin), blocking (i.e.: alerting and blocking), and deception (i.e.: alerting and redirect, honey destination, misleading response, etc.)

## Business Value

Blue teams and threat hunters burn valuable cycles tryng to understand where attackers dwell in their environments and how attackers are communicating externally to accomplish their missions. This solution aims to identify malicious activity ealry, as well as provide preventative and / or deceptive controls. This allows an organisation to be selective about how they want to respond and what feedback they want to provide the attackers; using deception will still be preventative but it could buy the responders time to investigate before alerting the adversaries. It is also intended that this provide high fidelity signals to teams for investigation so as to reduce alert fatigue and tick and flick alert investigation; increasing the organisations security posture while reducing the operation burden upon security operations teams.

## Technologies Used

Big-IP, Telemetry Streaming, iRules, ILX, Elastic Search, Kibana, Log Stash, Virus Total

## Presentations

#### VIDEO EXAMPLE:

Update the src link with the embedded link of your video.

<iframe width="560" height="315" src="https://web.microsoftstream.com/embed/video/471816ec-fc92-4488-aab7-6654b4714b2f?autoplay=false&showinfo=true" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

#### POWERPOINT EXAMPLE:

Update the src link with the embedded link provided by powerpoint under the share option.

<iframe src="https://f5.sharepoint.com/:p:/r/sites/F5HackfestFeb23/Shared%20Documents/Egress%20Control%20Dashboard%20and%20Security%20Operations/2023-02-03_hackfest_Egress_Control.pptx?d=wefd1630a9f9845ef9823ae2580e58979&csf=1&web=1&e=w00eTf" width="476px" height="288px" frameborder="0">This is an embedded <a target="_blank" href="https://office.com">Microsoft Office</a> presentation, powered by <a target="_blank" href="https://office.com/webapps">Office</a>.</iframe>

## Interested? Come join us!

Reach out to the principal researchers if you are interested in supporting this project.

| Role   | Skills                                                               |
| ------ | ------------------------------------------------------------------------- |
| example role  | example skills |

# Golkonda
