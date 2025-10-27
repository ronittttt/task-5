# task-5
Wireshark was used on Kali Linux to monitor live network activity through the active network interface. A capture session was started, and web browsing traffic was generated for roughly one minute to produce a range of packets. After stopping the capture, the Protocol Hierarchy view was opened to analyze the captured data and identify the main communication protocols used during the session.

Capture Summary

Total Packets Captured: 206

Primary Data Link Protocol: Ethernet

Network Layer Protocol: Internet Protocol Version 4 (IPv4)

Transport Layer Protocols: Transmission Control Protocol (TCP) and User Datagram Protocol (UDP)

Application Layer Protocols: Transport Layer Security (TLS) and Domain Name System (DNS)
| Protocol | Packets | Percent Packets | Bytes  | Percent Bytes |
| -------- | ------- | --------------- | ------ | ------------- |
| Ethernet | 206     | 100%            | 69,743 | 100%          |
| IPv4     | 206     | 100%            | 69,743 | 100%          |
| UDP      | 2       | 1.0%            | 16     | 0.0%          |
| DNS      | 2       | 1.0%            | 90     | 0.1%          |
| TCP      | 204     | 99.0%           | 66,161 | 94.9%         |
| TLS      | 64      | 31.1%           | 66,167 | 94.9%         |

Analysis

The captured data represents standard web browsing behavior. Almost all packets were transmitted using TCP, the dominant transport protocol for reliable communication. A substantial portion of the TCP traffic was encrypted using TLS, indicating that most web activity occurred over HTTPS connections. DNS traffic, carried via UDP, was minimal but necessary for resolving domain names before establishing web sessions.

The Ethernet and IPv4 layers served as the foundation for packet transmission, encapsulating all higher-level protocols. The large share of bytes associated with TLS suggests secure data exchanges, such as loading encrypted web pages. No abnormal or suspicious protocols were detected, and the traffic appears consistent with normal browsing activity.

Export

The entire capture was exported as a .pcap file for record-keeping and deeper inspection in future network analysis or reporting tasks.
