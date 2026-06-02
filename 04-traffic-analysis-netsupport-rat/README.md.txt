# Lab 04 — NetSupport Manager RAT Traffic Analysis

**Tool:** Wireshark  
**Source:** malware-traffic-analysis.net (2026-02-28)  
**Date:** June 2026

## Summary
Analysed a PCAP from a simulated SOC alert for NetSupport 
Manager RAT activity. Identified the infected host, MAC address, 
hostname, and user account using Wireshark filters for HTTP, 
NBNS, and Kerberos traffic.

## Wireshark Filters Used
- HTTP POST to C2: `(http.request or tls.handshake.type eq 1) and !(ssdp) and ip.addr eq 45.131.214.85`
- MAC/Hostname: `nbns`
- User account: `kerberos.CNameString`

## Skills Demonstrated
- PCAP analysis and triage
- NetBIOS and Kerberos protocol analysis
- IOC identification
- SOC incident report writing