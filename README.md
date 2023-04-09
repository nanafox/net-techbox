# The Network Technician's Toolbox

## What's in it?

![banner](https://bit.ly/3M9UaL6)

### **Network Reachability Testing Tools**

- **ping** (aliased to `ping -c 5`)
  - Supports both IPv4 and IPv6 testing
  - Pings are limited to 5 counts.
  - this behavior can be modified by editing the _~/.bash_aliases_ file
- **tscon** - An extended ping utility

  - Use this for more improved pings and options interatively

  ![tscon](https://bit.ly/431Ut0w)

- **traceroute**
- **tracepath**
  - Network path tracer. It also attempts to discover the MTU of the path
  - IPv4 and IPv6 support. See `tracepath6` on how to use if for IPv6 testing
- **tracepath6** (aliased to `tracepath -6`)
  - the original command syntax could be used as well. E.g. `tracepath -6 <destination>`
  - the aliased version is just for convenience sake.
    To use it the syntax looks like this `tracepath6 <destination>`
- **arp**
- **arping (ARP ping)**
  - Find the Layer 2 (MAC Address) address associated with Layer 3 (IP Address) address

### **Network Sniffing and Spoofing Tools**

- **nmap**

  - Here are a few aliases to make your task easier and not worry about the switches

    - netswp - Performs a ping sweep on the network addres 2received. E.g. `netswp 192.168.10.0/24`

    ![netswp](https://bit.ly/40CZ9bQ)

    - osscan - Performs an OS discovery. E.g. `osscan 192.168.10.30`

    ![osscan_cisco_router](https://bit.ly/40Bh2Yg)

- **tcpdump**
- **macof** (MAC Address Spoofing) - flood the local network with random MAC addresses.
  - great for testing Port Security
- **arpspoof** - Send out unrequested (and possibly forged) arp replies.
  - Dynamic ARP Inspection, DHCP Snooping
- **dnsspoof** - forge replies to arbitrary DNS address / pointer queries the Local Area Network.
- **dsniff** - password sniffer for several protocols.
- **filesnarf** - saves selected files sniffed from NFS traffic.
- **mailsnarf** - sniffs mail on the LAN and stores it in mbox format.
- **msgsnarf** - record selected messages from different Instant Messengers.
- **sshmitm** - SSH monkey-in-the-middle. proxies and sniffs SSH traffic.
- **sshow** - SSH traffic analyser.
- **tcpkill** - kills specified in-progress TCP connections.
- **tcpnice** - slow down specified TCP connections via "active"shaping.
- **urlsnarf** - output selected URLs sniffed from HTTP traffic in CLF.
- **webmitm** - HTTP / HTTPS monkey-in-the-middle. transparently proxies.
- **webspy** - sends URLs sniffed from a client to your local browser

### **Network Management and Monitoring Tools**

- **SSH**
- **SNMP**
  - inlcudes traps
- **Syslog**
- **DHCP Client**
- **FTP Server and Client**
  - SFTP Server (vsftpd)
  - TFTP client (tftp)
- **IP Address Calculator (ipcalc-ng)**
  - IPv4 and IPv6 support
- iptables
- ufw (Uncomplicaed Firewall)
- nftables

### Test Editors

- **Vim**
- **Nano**

## Lab Environments

This container works well in network simulation softwares

- Here is an example of it on GNS3
  ![gns3_lab](https://bit.ly/3G6nej2)
