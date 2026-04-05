\# Part 2: Subnetting Exercises



\### Exercise 1: Basic Subnetting

\*\*Network:\*\* 192.168.10.0/24

\*\*Goal:\*\* Divide into 4 equal subnets.

\*\*Math:\*\* A /24 has 256 IPs. $256 / 4 = 64$ IPs per chunk. This makes the mask a /26.



| Subnet # | Network Address | First Usable IP | Last Usable IP | Broadcast Address | Subnet Mask | CIDR |

| :--- | :--- | :--- | :--- | :--- | :--- | :--- |

| 1 | 192.168.10.0 | 192.168.10.1 | 192.168.10.62 | 192.168.10.63 | 255.255.255.192 | /26 |

| 2 | 192.168.10.64 | 192.168.10.65 | 192.168.10.126 | 192.168.10.127 | 255.255.255.192 | /26 |

| 3 | 192.168.10.128 | 192.168.10.129 | 192.168.10.190 | 192.168.10.191 | 255.255.255.192 | /26 |

| 4 | 192.168.10.192 | 192.168.10.193 | 192.168.10.254 | 192.168.10.255 | 255.255.255.192 | /26 |



\---



\### Exercise 2: Intermediate Subnetting (VLSM)

\*\*Base Network:\*\* 172.16.0.0/16



| Dept | Hosts | CIDR | Subnet Mask | Network ID | Broadcast | Wasted |

| :--- | :--- | :--- | :--- | :--- | :--- | :--- |

| \*\*Engineering\*\* | 200 | /24 | 255.255.255.0 | 172.16.0.0 | 172.16.0.255 | 54 |

| \*\*HR\*\* | 50 | /26 | 255.255.255.192 | 172.16.1.0 | 172.16.1.63 | 12 |

| \*\*Sales\*\* | 25 | /27 | 255.255.255.224 | 172.16.1.64 | 172.16.1.95 | 5 |

| \*\*Management\*\* | 10 | /28 | 255.255.255.240 | 172.16.1.96 | 172.16.1.111 | 4 |



\---



\### Exercise 3: Troubleshooting Scenario

1\. \*\*Subnet:\*\* The computer belongs to the \*\*192.168.1.128/26\*\* subnet.

2\. \*\*Valid Range:\*\* \*\*192.168.1.129 to 192.168.1.190\*\*.

3\. \*\*Communication:\*\* \*\*No\*\*, it cannot communicate with the gateway. The gateway (192.168.1.1) is in a different room (the 192.168.1.0/26 subnet). 

4\. \*\*Fix:\*\* Change the Default Gateway to an address within the same subnet (e.g., \*\*192.168.1.129\*\*) or change the subnet mask to \*\*255.255.255.0 (/24)\*\* so all devices are in one large room.

