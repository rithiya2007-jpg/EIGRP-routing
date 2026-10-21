# EIGRP Routing

## Project Overview
This Cisco Packet Tracer lab demonstrates Enhanced Interior Gateway Routing Protocol (EIGRP) across three routers connected in a chain. Each router connects to a local LAN, and the routing configuration allows devices on different LANs to communicate.

## Features
- Three-router chain topology.
- EIGRP dynamic routing configuration.
- Multiple IPv4 LAN networks.
- Router-to-router point-to-point links.
- End-to-end connectivity verification using ping.
- Troubleshooting using EIGRP neighbor and routing-table commands.

## Technologies Used
- Cisco Packet Tracer — network simulation.
- Cisco IOS CLI — router configuration.
- EIGRP — dynamic routing protocol.
- IPv4 — IP addressing and subnetting.
- ICMP — connectivity testing.

## Topology Notes
Visible labels in the supplied screenshot include:
- LAN networks: `192.168.2.0/24`, `192.168.3.0/24`, and `192.168.4.0/24`
- Example router LAN addresses: `192.168.2.1`, `192.168.3.1`, and `192.168.4.1`
- Router-to-router endpoint labels include `10.10.10.1`, `10.10.10.2`, `11.11.11.1`, and `11.11.11.2`

The screenshot shows successful ping replies to `192.168.2.2` and `192.168.3.2`.

## Project Structure
```text
EIGRP-Routing/
├── topology-and-ping-screenshot.jpg
└── README.md
```

## How to Recreate and Test
1. Recreate the topology from `topology-and-ping-screenshot.jpg` in Cisco Packet Tracer.
2. Configure IP addresses and subnet masks on all router interfaces and PCs.
3. Configure EIGRP with the same autonomous system number on all participating routers.
4. Advertise each connected LAN and router-to-router network.
5. Set each PC's default gateway to its local router LAN interface.
6. Ping devices on remote LANs to verify routing.

## Useful Verification Commands
```text
show ip interface brief
show ip eigrp neighbors
show ip route eigrp
show running-config
ping <destination-ip>
```

## Expected Result
If EIGRP, IP addressing, and default gateways are configured correctly, routers should form EIGRP neighbor relationships, learn remote LAN routes, and forward traffic between end devices.

## Important Note
This repository contains the screenshot and documentation prepared from the supplied image. The original `.pkt` file was not supplied. The visible labels do not show every subnet mask and interface setting, so verify the actual topology before applying any configuration.
