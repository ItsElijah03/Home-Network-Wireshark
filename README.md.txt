
Home Network Traffic Analysis Using Wireshark
Overview

This project documents a basic network analysis performed on my home network using Wireshark.
The objective was to capture live traffic, apply protocol filters, identify active devices, and observe how my system communicates on the network.
This hands-on exercise demonstrates foundational network analysis skills relevant to IT, cybersecurity, and troubleshooting roles.

Environment

Operating System: Windows 10

Tool: Wireshark (latest release)

Connection Type: Home Wi-Fi

Network Range Observed: 10.0.x.x

Methodology
1. Capture Setup

Launched Wireshark on Windows.

Selected my active network adapter (Wi-Fi).

Started a live packet capture.

2. Filters Applied

To focus the analysis, I used the following display filters:

Filter	Purpose
arp	Identify device presence and local network activity.
dns	View DNS lookups and identify domains being queried.
ip.addr == <my IP>	Isolate traffic specific to my system.
3. ARP Observation

The ARP filter was used to detect devices communicating on the LAN.
Only my network adapter’s ARP traffic appeared, which is normal when other devices are idle or not actively broadcasting.

4. DNS Observation

Using the dns filter, I captured DNS queries made by my system, including lookups for common domains and background service traffic.

5. Full Traffic Review

A short unfiltered capture was performed to observe:

TCP and UDP packet flows

Broadcast traffic

Device manufacturer identifiers

General network behavior

Devices on the Network

During the analysis period, these devices were active on my home network:

Windows Desktop PC (analysis machine)

iPhone

Roku TV

Two smartphones

Nintendo Switch

(Some devices did not produce visible ARP chatter during the capture window.)

Findings
✔ ARP Traffic

ARP packets mainly showed my own adapter announcing itself.

Manufacturer data reflected Intel/Microsoft address allocations (expected for a Windows system).

✔ DNS Queries

DNS lookups included routine service traffic (e.g., Google, Apple, Microsoft).

Verified proper DNS functionality and normal resolution patterns.

✔ Device Activity

My device generated the majority of recorded packets.

Traffic patterns were consistent with routine Windows background operations plus general browsing queries.

Screenshots

Screenshots included in the repository:

Description	File
ARP packet results	screenshots/arp_capture.png
DNS filter results	screenshots/dns_capture.png
Full capture with no filter	screenshots/full_traffic.png

(All sensitive details such as private IP addresses or MAC addresses are blurred.)

What I Learned

How to identify network devices using ARP broadcasts.

How to isolate packets by filtering for specific protocols.

How DNS traffic appears in packet captures and how to interpret it.

How to document network observations for technical review or analysis reports.