# Task-1-Scan-your-Local-networks-for-open-ports
## Introduction
In this project, you will learn how to use Nmap, a powerful network scanning tool, to discover devices and services running on a local network. Network scanning and enumeration are critical skills for ethical hackers, as they help in identifying potential targets and vulnerabilities within a network. By the end of this project, you will be able to perform basic network scans, identify open ports, and gather information about the devices on your network using Kali Linux.

## Pre-requisites
- Basic understanding of networking concepts (IP addresses, ports, etc.).
- Familiarity with using the command line interface (CLI).
- Kali Linux installed on your machine (either natively, on a virtual machine, or as a live boot).


## Lab Set-up and Tools

### Tools
- **Kali Linux**: A Debian-derived Linux distribution designed for digital forensics and penetration testing.
- **Nmap**: Network exploration tool and security/port scanner (pre-installed on Kali Linux).
- A local network with multiple devices connected (computers, printers, IoT devices, etc.).

### Installation
Nmap is pre-installed on Kali Linux. You can verify the installation or update it using the following command:
```sh
sudo apt-get update && sudo apt-get install nmap
```

## Tasks
In kali linux terminal

# Task-1-Scan-your-Local-networks-for-open-ports
## Introduction
In this project, you will learn how to use Nmap, a powerful network scanning tool, to discover devices and services running on a local network. Network scanning and enumeration are critical skills for ethical hackers, as they help in identifying potential targets and vulnerabilities within a network. By the end of this project, you will be able to perform basic network scans, identify open ports, and gather information about the devices on your network using Kali Linux.

## Pre-requisites
- Basic understanding of networking concepts (IP addresses, ports, etc.).
- Familiarity with using the command line interface (CLI).
- Kali Linux installed on your machine (either natively, on a virtual machine, or as a live boot).

## Lab Set-up and Tools

### Tools
- **Kali Linux**: A Debian-derived Linux distribution designed for digital forensics and penetration testing.
- **Nmap**: Network exploration tool and security/port scanner (pre-installed on Kali Linux).
- A local network with multiple devices connected (computers, printers, IoT devices, etc.).

### Installation
Nmap is pre-installed on Kali Linux. You can verify the installation or update it using the following command:
```sh
sudo apt-get update && sudo apt-get install nmap
```

## Tasks
In kali linux terminal
# Scan Your Local Network for Open Ports
**. Objective:** Learn to discover open ports on devices in your local network to understand network exposure.

**. Tools:** Nmap (free), Wireshark (optional)

## 1. Install Nmap from official website

nmap is pre installed tool in kali for check run this command

> nmap -h
> 

<img width="955" alt="image" src="https://github.com/user-attachments/assets/59e3ef0e-ad1f-4076-9c6d-53e29c0f71e4" />

## 2.Find your local IP range command;

> ip a
> 
> 
> ifconfig
> 

<img width="959" alt="image" src="https://github.com/user-attachments/assets/adcf3f83-c1fb-4884-82fd-b3e69bf75f57" />


## 3.Run: nmap -sS 192.168.1.0/24 to perform TCP SYN scan

<img width="959" alt="image" src="https://github.com/user-attachments/assets/074d5c29-c600-4bc0-982f-c949d65adb24" />


## 4.Note down IP addresses and open ports found.

**. Detailed Results :**

192.168.29.66 -  this port is typically used for DNS (Domain Name System)

All 1000 scanned ports are filtered

Port 3306/tcp is filtered 

192.168.29.246

The remaining 999 ports are closed, which means the system received the request but actively rejected the connection

192.168.29.178

All 1000 scanned ports are filtered

This is most likely a router or firewall-protected device that blocks incoming scan requests

192.168.29.178 (Your own system)

All 1000 scanned ports are in ignored state.

This indicates that the scan reached the system, but all ports rejected the connection attempts

## 5.Optionally analyze packet capture with Wireshark

<img width="959" alt="image" src="https://github.com/user-attachments/assets/975ec83d-1f68-4560-978e-5172923c16ac" />


## 6.Research common services running on those ports.

there is no services running because off no port is running

## 7.Identify potential security risks from open ports.

i have nothing found suspicious on this services because off no port is open

## 8.Save scan results as a text or HTML file.

here i save these output in test file like nmap.txt

comand;

> nmap -sS 192.168.117.0/24 -oN nmap.txt
> 

<img width="958" alt="image" src="https://github.com/user-attachments/assets/510e14d7-f53d-4486-a906-c3a533ab4acc" />


scan of result in nmap.txt file

<img width="956" alt="image" src="https://github.com/user-attachments/assets/b4dccba8-0fea-4759-a120-33a3d173c22b" />


