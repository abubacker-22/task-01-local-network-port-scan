# Task 1 – Scan Local Network for Open Ports

## Objective

To perform basic network reconnaissance on a local VirtualBox NAT network using Nmap, identify active hosts, discover open TCP ports, identify associated services, and document potential security considerations.

## Environment

- Operating System: Kali Linux
- Network Type: VirtualBox NAT
- Network Range: 10.0.2.0/24
- Kali Linux IP: 10.0.2.15
- Default Gateway: 10.0.2.2
- Tool: Nmap 7.99

## Scope

This scan was performed within my Kali Linux VirtualBox NAT lab environment using the 10.0.2.0/24 network. The assessment was limited to this controlled environment.

## Network Discovery

The local network was identified using:

```bash
ip addr
ip route
