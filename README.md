TCP SYN Flood Incident Report

Short description
Analysis of a TCP SYN Flood (DoS) attack that caused the company web server to become unresponsive by flooding it with incomplete TCP connection requests.

Evidence (summary)
Packet captures show repeated SYN packets to port 443 from 203.0.113.0 with no completing ACK.
Server replied SYN-ACK repeatedly and accumulated half-open connections, causing timeouts and 504 errors.

Impact
Website unavailable / connection timeout for users and employees.
Lost productivity and potential revenue; reputational damage risk.

Mitigation & Recommendations
Enable SYN cookies and shorten TCP SYN timeout.
Apply rate limiting and connection throttling on perimeter devices.
Deploy IDS/IPS and a DDoS mitigation service (CDN or cloud-based scrubbing).
Monitor and block malicious IPs temporarily; investigate for IP spoofing or DDoS amplification sources.
