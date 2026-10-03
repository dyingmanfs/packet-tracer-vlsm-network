# Packet Tracer VLSM Network Design

A Cisco Packet Tracer project focused on IP addressing, VLSM subnetting, supernetting, dynamic routing, and multi-router network design.

## Overview

This project designs and implements a structured enterprise-style network using Cisco Packet Tracer.

The network contains multiple workgroups with different host requirements, including:

- Classrooms
- Student accommodation
- Staff networks
- Laboratories
- Administration networks
- Point-to-point serial links

The IP addressing scheme was designed using **VLSM (Variable Length Subnet Masking)** to allocate address space efficiently.

## Network Design

The project includes:

- VLSM-based subnet planning
- Network, broadcast, first host, and last host address calculations
- Supernetting for summarized routing
- /30 subnets for point-to-point serial connections
- Multiple routers and switches
- Separate LANs for different organizational units
- Dynamic routing using RIPv2

## Routing

RIPv2 was configured on the routers to allow communication between all subnets.

Auto-summary was disabled to support the VLSM-based addressing structure.

Connectivity between different networks was verified using ping tests.

## Example Subnets

Some of the implemented networks include:

| Network | Subnet |
|---|---|
| Classroom 1 | 210.30.8.0/24 |
| Classroom 2 | 210.30.9.0/24 |
| Student Accommodation 1 | 210.30.10.0/25 |
| Student Accommodation 2 | 210.30.10.128/25 |
| Staff 1 | 210.30.11.0/26 |
| Staff 2 | 210.30.11.64/26 |
| Lab 1 | 210.30.11.128/26 |
| Lab 2 | 210.30.11.192/26 |
| Administration 1 | 210.30.12.0/27 |
| Administration 2 | 210.30.12.32/27 |
| Serial Link 1 | 210.30.12.64/30 |
| Serial Link 2 | 210.30.12.68/30 |

## Network Summary

A summarized address was calculated to reduce routing complexity:

```text
210.30.8.0/21
