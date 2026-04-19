# TCP/UDP Network Analyzer and RTT Measurement

## 📌 Overview
This project focuses on implementing and analyzing TCP and UDP communication using Python sockets in a Linux environment.

The goal is to understand how data is transmitted over networks, how different protocols behave, and how network conditions such as packet loss affect performance.

---

## 🎯 Objectives
- implement client-server communication using UDP and TCP
- capture and analyze packets using Wireshark
- simulate packet loss and observe protocol behavior
- measure round-trip time (RTT) at application level
- compare application-level RTT with system-level ping

---

## 🛠️ Technologies Used
- Python (socket programming)
- Linux
- Wireshark
- tc (traffic control for packet loss simulation)

---

## ✅ Main Experiments and Results

### 1. UDP Communication
A UDP client and server were implemented using Python sockets.

The client sent multiple packets to the server, each containing:
- a message string
- a sequence number

The server received packets using `recvfrom()` and printed their content.

**Key observations**
- UDP is connectionless
- packets are sent without handshake
- no guarantee of delivery or order

---

### 2. Packet Analysis with Wireshark
Wireshark was used to capture UDP traffic using filters such as:

```bash
udp.port == 47999
