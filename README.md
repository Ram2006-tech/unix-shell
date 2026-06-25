# C-Shark – The Command-Line Packet Predator

A command-line packet analyzer built in **C** using **libpcap** for capturing, decoding, and inspecting live network traffic. C-Shark performs multi-layer protocol analysis from Ethernet frames to application-layer protocols, supports protocol-based filtering, and provides interactive packet inspection with hexadecimal and ASCII visualization.

---

## Features

- Live packet capture from available network interfaces
- Automatic network interface discovery
- Multi-layer packet decoding
- Interactive command-line interface
- Protocol-based packet filtering
- Session storage for offline inspection
- Hexadecimal and ASCII packet visualization
- Graceful signal handling (`Ctrl+C` and `Ctrl+D`)

---

## Supported Protocols

### Layer 2
- Ethernet
- ARP

### Layer 3
- IPv4
- IPv6

### Layer 4
- TCP
- UDP

### Application Layer
- HTTP
- HTTPS
- DNS

---

## Packet Analysis

C-Shark extracts and displays protocol-specific information for every captured packet.

### Ethernet
- Source and Destination MAC Addresses
- EtherType

### IPv4
- Source and Destination IP
- TTL
- Protocol
- Packet ID
- Header Length
- Total Length
- Fragmentation Flags

### IPv6
- Source and Destination IP
- Traffic Class
- Flow Label
- Payload Length
- Next Header
- Hop Limit

### ARP
- Operation Type
- Sender and Target IP Addresses
- Sender and Target MAC Addresses
- Hardware and Protocol Information

### TCP
- Source and Destination Ports
- Sequence Number
- Acknowledgement Number
- Flags
- Window Size
- Header Length
- Checksum

### UDP
- Source and Destination Ports
- Datagram Length
- Checksum

### Payload Inspection
- HTTP Detection
- HTTPS Detection
- DNS Detection
- Hex + ASCII dump of packet payload

---

## Packet Filtering

C-Shark supports protocol-based packet filtering including:

- HTTP
- HTTPS
- DNS
- TCP
- UDP
- ARP
- Custom IP filters
- Custom Port filters

---

## Session Management

Captured packets are stored during execution for later inspection.

Features include:

- Packet history
- Session persistence
- Detailed packet inspection
- Packet summary table
- Memory management for up to **10,000 packets**

---

## Requirements

- Linux
- GCC
- libpcap

Install libpcap on Ubuntu/Debian:

```bash
sudo apt install libpcap-dev
```

---

## Build

```bash
make clean
make
```

---

## Run

```bash
sudo ./cshark
```

> **Note:** Root privileges are required for live packet capture.

---

## Example Workflow

1. Select a network interface.
2. Start packet capture.
3. Capture all packets or apply protocol filters.
4. Stop capture using **Ctrl+C**.
5. Inspect captured packets.
6. View detailed packet information.
7. Exit the application.

---

## Technologies Used

- C
- libpcap
- POSIX APIs
- Linux Networking

---

## Concepts Demonstrated

- Packet sniffing using libpcap
- Network protocol parsing
- Layer-by-layer packet analysis
- Binary data processing
- Memory management
- Signal handling
- Interactive terminal applications
- Hexadecimal packet visualization

---

## Project Structure

```
.
├── include/
├── src/
├── Makefile
└── README.md
```

---

## Future Improvements

- PCAP file export
- ICMP and ICMPv6 support
- IPv6 extension header parsing
- Packet statistics dashboard
- Enhanced filtering options
- Colored terminal output

---

## License

Developed for educational purposes as part of a systems programming course.