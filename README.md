# DNS & DHCP Server Setup 
 
## Problem Statement

Employees' computers required manual static IP configuration, making network administration time-consuming. Additionally, employees had to remember the intranet server's IP address to access the company's internal website.

## Solution

This project implements centralized DHCP and DNS services using Cisco Packet Tracer.

- **Server 1 – DHCP:** Automatically assigns IP addresses and network configuration to employee computers.
- **Server 2 – DNS & HTTP:** Resolves `intranet.company.local` to the web server's IP address and hosts the company's internal website.

## IP Addressing Scheme

| Device | IP Address |
| Router (Default Gateway) | 192.168.10.1 |
| Server 1 (DHCP) | 192.168.10.2 |
| Server 2 (DNS & HTTP) | 192.168.10.3 |
| Employee PC 1 | DHCP |
| Employee PC 2 | DHCP |
| DHCP Pool | 192.168.10.100 – 192.168.10.200 |

**Subnet Mask:** `255.255.255.0`

**Default Gateway:** `192.168.10.1`

**DNS Server:** `192.168.10.3`

## Project Implementation

1. Designed the corporate LAN topology in Cisco Packet Tracer.
2. Configured the router as the default gateway.
3. Assigned static IP addresses to both servers.
4. Configured DHCP to automatically assign IP addresses.
5. Configured DNS with the record `intranet.company.local`.
6. Enabled HTTP service on Server 2.
7. Configured employee PCs to obtain IP addresses automatically.
8. Tested network connectivity and intranet access.

## Testing and Verification

The following tests are performed:

- DHCP lease verification using `ipconfig`.
- Router connectivity using `ping`.
- Intranet accessibility using the PC web browser.

Screenshots of the actual implementation are available in the `Screenshots/` directory.

## Technologies Used

- Cisco Packet Tracer
- DHCP (Dynamic Host Configuration Protocol)
- DNS (Domain Name System)
- HTTP (Hypertext Transfer Protocol)
- IPv4 Networking 

## Conclusion

This project demonstrates how DHCP and DNS simplify corporate network administration. Employee computers receive network configurations automatically, while DNS allows users to access the internal company website using a memorable domain name instead of an IP address.
