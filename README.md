## Overview

Wi-Fi deauthentication frames are management frames used to signal that a wireless station's association has ended. This project is intended to help learners understand how these frames are structured and how wireless clients may respond to them.

## Features

- Builds IEEE 802.11 deauthentication frame objects with Scapy.
- Demonstrates the roles of RadioTap, 802.11 MAC headers, and deauthentication reason codes.
- Supports learning and analysis in an authorized, isolated wireless lab.

## Requirements

- Python 3
- Scapy
- A Linux environment is recommended for wireless experimentation.
- Wireless adapter and driver capabilities vary; monitor-mode support does not necessarily mean frame injection is supported.

## Installation

Create and activate a virtual environment:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Install Scapy:

```bash
python -m pip install scapy
```

## Usage

Use this project for packet inspection and controlled lab exercises. Start by constructing a frame and inspecting its fields with Scapy's `show()` method, or analyze an existing capture in Wireshark.

For example, a deauthentication frame's reason code can be inspected in Wireshark after opening an authorized capture. The IEEE 802.11 reason code `7` means **“Class 3 frame received from a nonassociated station.”**

This repository's description and examples should not be taken as a guarantee that a frame will be transmitted, received, or accepted by a client. Outcomes depend on the adapter, driver, network configuration, and protections such as Protected Management Frames (PMF).

## Safety and Legal Notice

**Use only in a wireless lab you own or have explicit permission to test.** Sending forged management frames can interrupt network connectivity for other users and devices. Do not use this project to disrupt public, organizational, or third-party networks.

Prefer an isolated test access point and dedicated test client. For demonstrations on a network you administer, use the router's management interface or instructor-approved lab procedures where appropriate.

## Background

- [Scapy documentation](https://scapy.readthedocs.io/)
- [Wireshark Sample Captures](https://wiki.wireshark.org/SampleCaptures)
- [Wi-Fi Alliance — Wi-Fi security](https://www.wi-fi.org/discover-wi-fi/security)

## Disclaimer

This project is provided for educational and authorized security-testing purposes only. You are responsible for complying with applicable laws, regulations, and network policies.
"""
path = Path("/mnt/data/README.md")
path.write_text(content, encoding="utf-8")
print(f"Created: {path}")
