# Secure Network Design and Simulation

## Overview

This project presents a communication security network design and simulation using Cisco Packet Tracer. It demonstrates how an Access Control List (ACL)-based firewall can restrict unauthorized access to an internal server while permitting legitimate user traffic.

## Objectives

- Design a secure network architecture using security zones.
- Configure an ACL-based firewall on a Cisco router.
- Allow authorized remote-user traffic.
- Block unauthorized traffic from an attacker.
- Evaluate firewall behavior using connectivity tests and ACL match counters.

## Technologies Used

- Cisco Packet Tracer
- Cisco IOS CLI
- Extended Access Control Lists (ACLs)
- IP addressing and routing
- Network security principles

## Network Configuration

| Device | IP Address |
|---|---|
| Remote User PC | `192.168.1.10` |
| Attacker PC | `192.168.1.20` |
| Router G0/0 | `192.168.1.1` |
| Router G0/1 | `192.168.2.1` |
| Internal Server | `192.168.2.10` |

## Security Implementation

The router uses an extended ACL named `FIREWALL_ACL` to filter traffic entering interface G0/0.

- **Rule 10:** Denies traffic from the attacker IP address.
- **Rule 20:** Permits traffic from the authorized remote user.
- **Rule 30:** Permits other traffic according to the configured ACL.

## Simulation Results

- **Authorized access:** The remote user successfully reaches the internal server; 3 out of 4 ping packets are received in the recorded test.
- **Unauthorized access:** The attacker's ping traffic is blocked, resulting in 100% packet loss in the recorded test.
- **ACL verification:** The recorded match counters show four matches for the deny rule and four matches for the permit rule.

## Repository Structure

- `docs/` — Project documentation and report.
- `simulation/` — Cisco Packet Tracer simulation file.
- `images/` — Network diagram and simulation evidence.

## Limitations

The simulation demonstrates ACL-based access control. Full VPN, TLS, and IDS/IPS functionality was not implemented or validated in Packet Tracer as part of this simulation.

## How to Run

1. Install Cisco Packet Tracer.
2. Download or clone this repository.
3. Open `simulation/secure-network-topology.pkt` in Cisco Packet Tracer.
4. Inspect the router configuration and repeat the authorized and unauthorized connectivity tests.

## Academic Project

Communication Security  
Department of Telecommunications Engineering  
NED University of Engineering and Technology, Karachi
