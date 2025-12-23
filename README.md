# Low-Impact-TCP-SYN-Scanning-CLI-Based-
This repository documents a controlled network analysis exercise focused on identifying TCP probing behavior using command-line tools only.

## Scope
- Target: Home router (192.168.1.1)
- Network: Local LAN
- Tools: nmap, tcpdump, tshark

## Approach
A minimal TCP SYN scan was performed against a limited port set (22, 80, 443) using long delays and low retry counts.  
Traffic was captured in real time to validate TCP behavior at the packet level.

## Key Observations
- Open port responded with SYN-ACK followed by client RST
- Closed ports returned immediate RST
- No full TCP sessions were established
- Traffic volume remained stable

## Conclusion
The observed traffic patterns confirm intentional probing rather than normal application traffic.  
The analysis demonstrates how low-impact scanning can be verified without aggressive techniques or GUI tools.

## Tools
- nmap
- tcpdump
- tshark

## Focus
Packet behavior, TCP flags, and response timing rather than alert-based assumptions.

 ## Lessons Learned

Traffic volume alone is not a reliable indicator of scanning activity

TCP flag sequences provide more accurate insight than port states alone

A SYN scan can remain almost invisible when timing and retries are controlled

Packet-level validation prevents false assumptions based on tool output

Not every scan requires aggressive options like -A or service detection

Understanding when to stop is as important as knowing how to scan
