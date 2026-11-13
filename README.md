# Network Scanning and Host Discovery

## Introduction

This project contains the practical networking and cybersecurity tasks I carried out during my learning. I used Windows Command Prompt, Nmap and Zenmap to understand network configurations and discover devices connected to a network.

## Objectives

- Understand IP addresses and network adapters.
- Identify my PC's IP address.
- Understand subnet masks and LAN subnets.
- Discover live hosts on a network.
- Learn how to identify MAC addresses.
- Practise network scanning with Nmap and Zenmap.

## Tools Used

- Windows Command Prompt (CMD)
- Nmap
- Zenmap
- Windows Network Configuration

## Practical Activities

### 1. Checking Network Configuration

I used the command below to view the network adapters and IP configurations on my PC.

```cmd
ipconfig /all
```

I discovered that my PC had multiple network adapters, each with different IP addresses.

Some of the addresses I identified were:

- 192.168.99.1
- 172.20.10.4
- 192.168.73.1
- 172.22.144.1

### 2. Identifying My LAN Subnet

For my active Ethernet connection, I identified:

- IP Address: 172.20.10.4
- Subnet Mask: 255.255.255.240
- Default Gateway: 172.20.10.1
- Network Subnet: 172.20.10.0/28

I learned that /28 provides 16 total IP addresses, with 14 usable host addresses.

### 3. Network Scanning With Zenmap

I used Zenmap to scan a network and identify active devices.

The initial scan was:

```bash
nmap -sn 192.168.99.0/24
```

I discovered that only one host was detected on that subnet:

192.168.99.1

### 4. Discovering Live Hosts

After identifying my active LAN subnet, I performed another scan:

```bash
nmap -sn -PR 172.20.10.0/28
```

The scan discovered two live hosts.

**Results:**

| IP Address   | Status     |
| ------------ | ---------- |
| 172.20.10.1  | Host is up |
| 172.20.10.12 | Host is up |

Total hosts discovered: 2.

### 5. MAC Address Identification

During the scan, I was able to identify one MAC address.

IP Address: 172.20.10.1

MAC Address: 9E:64:8B:93:41:64

The MAC address for 172.20.10.12 was not displayed.

I learned that MAC addresses help identify network interfaces and that Nmap can display them during local network discovery.

## Nmap Commands Learned

```bash
nmap -sn 192.168.99.0/24
nmap -sn -PR 172.20.10.0/28
```

Other useful Windows command:

```cmd
ipconfig /all
```

## Challenges Faced

- I initially had difficulty finding my PC's MAC address in Zenmap.
- My PC had multiple network adapters, which made identifying the correct IP address confusing.
- I encountered an Nmap error while entering a scan command.
- I had to identify the correct subnet before performing the final scan.

## What I Learned

From this practical, I learned how to check network configurations, identify IP addresses, understand subnet masks, discover live hosts and retrieve MAC addresses using Nmap.

I also understood why identifying the correct network adapter is important before scanning a network.

## Conclusion

This practical helped me understand basic network reconnaissance and how network scanning works. I gained practical experience using Nmap and Zenmap and improved my understanding of IP addressing, subnetting and host discovery.

## Author

Aimuanmwosa Melissa

Focus: Cybersecurity, Ethical Hacking and Linux

Project: Network Scanning and Host Discovery
## Screenshots

### 1. Network Configuration
![Network Configuration](<screenshots/Screenshot (942).png>)

### 2. Network Adapter Information
![Network Adapters](<screenshots/Screenshot (943).png>)

### 3. Initial Network Scan
![Initial Scan](<screenshots/Screenshot (944).png>)

### 4. Live Host Discovery
![Live Host Discovery](<screenshots/Screenshot (947).png>)
