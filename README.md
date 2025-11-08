# Mikrotik Laodbalncing-Complete-Guide

![GitHub](https://img.shields.io/github/license/kaoheng1515/loadbalancing_2ISP?style=flat)
![GitHub last commit](https://img.shields.io/github/last-commit/kaoheng1515/loadbalancing_2ISP?style=flat)
![ViewCount](https://views.whatilearened.today/views/github/kaoheng1515/loadbalancing_2ISP.svg?cache=remove)

<br>

[![telegram (1)](https://github.com/hegdepavankumar/VMware-ESXi-License-Keys/assets/85627085/cbc449b9-ddda-4d84-8c5e-5c77e29f89ed)](https://t.me/server_networ_opensource)

<br>

# Topics to be covered:

---

| No | Name                                                                   |
| --- | ----------------------------------------------------------------------------|
| Step 1   | [**Add IP Route**](#introduction-to-fortigate-firewall) |
| Step 2   | [**Add Routing table**](#interface-configurations-and-firewall-policies) | 
| Step 3   | [**Add Mangle roles**](#high-availability) |
| Step 4   | [**Input ISP1**](#firewall-authentication) |
| Step 5   | [**Input ISP2**](#security-profiles) |
| Step 6   | [**Output ISP1**](#logging-and-monitoring) |
| Step 7   | [**Output ISP2**](#basic-ipsec-vpn) |
| Step 8   | [**Add Route to ISP**](#ssl-vpn)  Upcoming..| 
| Step 9   | [****](#Upcoming) Upcoming.. |

# Getting Started: 
  ## Information ISP 1&2
    1. ISP1 Ip address 49.156.43.94/29 Default Gateway 49.156.43.89
    2. ISP2 Ip address 96.9.66.101/25 Default Gateway 96.9.66.101
# Step1 Add IP Route

  ### Add Route ISP1
  **Click on IP: Route —> Add**
  - **Destination**: 0.0.0.0/0
  - **Gateway**: 49.156.43.89
  - **Distance**: 1
  - **Check Gateway**: Ping
  - **Click OK**

  ```markdown
    /ip route add dst-address=0.0.0.0/0 gateway=49.156.43.89 check-gateway=ping distance=1
  ```
 ## Image:
    
  ### Add Route ISP2
  **Click on IP: Route —> Add**
  - **Destination**: 0.0.0.0/0
  - **Gateway**: 96.9.66.1
  - **Distance**: 1
  - **Check Gateway**: Ping
  - **Click OK**
    /ip route add dst-address=0.0.0.0/0 gateway=96.9.66.1 check-gateway=ping distance=1

    

    
