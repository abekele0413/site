---
permalink: netsec-spheres-of-support-for-dedicated-and-managed-ops
title: NetSec Spheres of Support
type: article
created_date: '2019-02-25'
created_by: Adrian Bekele
last_modified_date: '2019-02-25'
last_modified_by: Adrian Bekele
product: Dedicated Hosting
product_url: dedicated-hosting
---

The Spheres of Support lists the technologies and features in the Network Security domain and defines support level for each item. It applies to Enterprise, SMB, US, International, unless otherwise noted.

Note that International NetSec also supports devices and technologies that are maintained by Security Support in the US. The support level of these features is described separately in Security Support Spheres of Support.


### Terminology

*  Supported - setup, configuration and troubleshooting.
*  Partial - setup, limited types of configuration and full troubleshooting of the supported configurations.
*  Reasonable endeavor - setup, attempt of configuration and attempt of troubleshooting.
   *   Use warning below when configuring a reasonable endeavor feature. 
*  Not supported - no setup or configuration provided.
   *   If an unsupported feature has to be supported on a device, this one-off has to be mentioned in the DMG by the Account Manager or the Lead Tech.
    
    
### Firewalls

|   | Feature | Cisco ASA | Juniper SRX |
| :---: |:--- | :---: | :---: |
| **Interfaces** |VLAN tagged (Cisco trunk)| ✓ | ✓ |
||VLAN untagged (Cisco access)| ✓ | ✓ |
||LACP bundling with number of interfaces is a power of 2| ✓ | ✓ |
| **Routing** |Static routing| ✓ | ✓ |
||Static routing with IP SLA tracking| ✓ |  |
| **IPv6** |Static routing| ✓ | ✓ |
||Static routing with IP SLA tracking| ✓ |  |
| **NAT** |Static (one-to-one)| ✓ | ✓ |
||PAT (NAT overloading)| ✓ | ✓ |
||Policy NAT/PAT| ✓ | ✓ |
||DNS Doctoring| ✓ | ✓ |
||Connection limits via static NAT| ✓ |  |
| **Packet filtering** |Layer 3/4 filtering ingress/egress| ✓ | ✓ |
||FQDN based filtering| ✓ | ✓ |
||Outbound ACL| ✓ |  |
| **DDoS Mitigation** |Connection limiting (Embryonic and/or established)  |✓| ✓|
||Connection timeouts |✓| ✓|
||TCP normalization modification  || ✓|
||Application inspection  || ✓|
| **VPN** |Route-based VPNs - BGP  |✓| ✓|
||Route-based VPNs - Static |✓| ✓|
||IPsec - IKEv2 L2L with PSK  |✓| ✓|
||IPsec LAN-to-LAN Layer 3/4 filtering  |✓| ✓|
||IPsec LAN-to-LAN Pre-shared keys authentication |✓| ✓|
||IPsec LAN-to-LAN Hub and spoke configuration  |✓| ✓|
||IPsec remote access with group authentication |✓| |
||IPsec remote access with group and user authentication  |✓| |
||IPsec remote access with two-factor authentication  |✓| |
||IPsec remote access - Multiple VPN groups |✓| |
||IPsec remote access with layer 3/4 filtering  |✓| |
||IPsec remote access - Split-tunneling |✓| |
||IPsec remote access - all traffic through VPN (tunnel all)  |✓| |
||IPsec remote access - DNS server assignment |✓| |
||IPsec remote access - Client certificate-based authentication || |
||SSL VPN AnyConnect Plus |✓||
||SSL VPN - Mobile client (Plus license feature)  |✓||
||SSL VPN - Two-factor authentication |✓||
| **Management** |  Buffered Logging  |✓| ✓|
||Log shipping to log correlation device within customer's account  |✓| ✓|
||SNMP read-only for customer |✓| ✓|
| **High Availability (HA)** |  Active/Standby (stateful and non-stateful) (clustering - SRX)<Br/>ASA 5510 and above, ASA-X 5508, 5515 and above |✓|✓|
| **Modes and modules** | Mode - Multi-Context Routed |✓||
||Mode - Routed |✓| ✓|
| **RackConnect** | RackConnect VLANs termination |✓| |
| **RackConnect Global** |  RackConnect Global Classic Static |✓| ✓|
||RackConnect Global 2.0 Static - BGP |✓| |
||RackConnect Global 2.1 Static - BGP (with TOR)  |✓| |


### Load balancers

| | Feature | F5 LTM | Brocade ADX | NetScaler VPX^ | NetScaler MPX^^|
| :---: |:--- | :---: | :---: | :---: | :---: |
| **Interfaces** |  VLAN tagged (Cisco trunk) |✓|✓||✓|
||VLAN untagged (Cisco access)  |✓|✓|✓|✓|
| **Routing** | Static Routes |✓|✓|Default route|✓|
| **IPv6** |  Static Routes |✓|✓| Default route|✓|
| **Packet filtering** |  Layer 3/4 Ingress/Egress |US - ✓ <Br/>Intl - X|✓|||
| **NAT** | Static (one-for-one)  |✓|✓|||
||PAT (NAT overload)  |✓|✓|||
||Source NAT pools on Virtual Servers |✓|✓|✓|✓|
| **Load balancing** |  Local Servers Servers behind the LB |✓|✓||✓|
||Remote Servers in front of the LB |✓|✓|✓|✓|
||Parallel Servers sitting as a neighbor to the LB  |✓|✓|✓|✓|
||Algorithms - Static (Round Robin or Weighted Round Robin) |✓|✓|✓|✓|
||Algorithms - Dynamic (Least Connections)  |✓|✓|✓|✓|
||Healthchecks - ICMP echo  |✓|✓|✓|✓|
||Healthchecks - Layer 4 TCP (Port Socket Check) and UDP (Port Rejection) |✓|✓|✓|✓|
||Healthchecks - Layer 7 HTTP (Response Code, String Search, Checks on non well-known ports)  |✓|✓|✓|✓|
||Healthchecks - Layer 7 HTTPS (SSL hello, Response Code, String Search, Checks on non well-known ports)  |✓|✓|✓|✓|
||TCP/UDP Virtual Servers (Catchall, Single Port) |✓|✓|✓|✓|
||SNAT  |✓|✓|✓|✓|
||HTTP Redirects  |✓|✓|✓|✓|
||URI Load Balancing  |✓|✓|✓|✓|
||SSL Offloading  |✓|✓|✓|✓|
||Pools - Single Node: port combination (multiple ports on a server)  |✓|✓|✓|✓|
||Pools - Connection Limits (Pool, Node)  |✓|✓|✓|✓|
||Pools - Priority Group Activation |✓||||
||LB - Pools - Group monitor applied to all pool members  |✓||✓|✓|
||LB - Pools - Individual monitors applied to each pool member  |✓|✓|✓|✓| 
||LB - Pools - Combination of individual and group monitors across different pool members |✓||✓|✓|
||LB - Application Profiles - HTTP (OneConnect, Custom HTTP Profile settings) |✓||✓|✓|
||LB - Application Profiles - SSL (Client and Server) |✓|✓|✓|✓|
||LB - Application Profiles - FTP (Active and Passive)  |✓||✓|✓|
||Persistence - TCP - Source IP |✓|✓|✓|✓|
||Persistence - HTTP cookie: LB generated, server generated |✓|✓|✓|✓|
||Persistence - HTTP Custom cookie name |✓||✓|✓|
||Persistence - Cookie encryption |✓||✓|✓|
||Persistence - UDP - Source IP |✓|✓|✓|✓|
||LB - Virtual Servers - SNAT Pools |✓|✓|✓|✓|
| **Scripting** | iRule 0006  |✓||||
| **Management** |  Logging - Local Buffered Logging  |✓|✓|✓|✓|
||Logging - Log shipping to log correlation device (Within customer's account)  |✓|✓|✓|✓|
||Management - SNMP read-only for customer  |✓|✓|✓|✓|
| **High availability (HA)** |  High availability |✓ 1600 and above  |✓ ADX 1000 only |✓|✓|
||HA - Active/Standby |✓|✓|✓|✓|
| **Modes and Modules** | Routed (Single and Multiple Route Domains) Default gateway for back end servers |✓|✓||✓|
||Routed (Single and Multiple Route Domains) t the default gateway for back end servers |||||
||Multiple Segments behind LB |✓|✓||✓<Br/>Interface filtering is |
| **RackConnect** | RackConnect VLANs termination |✓|RCV2 - X<Br/>RCv3 - ✓|||
| **RackConnect Global** |  RackConnect Global Classic Static |✓(AFM only)||||
| **SSL VPNs** |  SSL Client VPN on edge Big-IPs using APM module |✓||||
| **SNI** | Server Name Indication  |✓|✓|✓|✓|

^ VPX - Product in EA soon to be LA

^^ MPX - Product not launched, supportability is only planned at this stage.
  
### Global load balancer

|| Feature | F5 GTM |  ADX GSLB | NetScaler VPX | NetScaler MPX|
| :--- |:--- | :---: | :---: | :---: | :---: |
| **Interfaces** |  VLAN tagged (Cisco trunk)|✓||||
||VLAN untagged (Cisco access)  |✓| |||     
||LACP bundling with number of interfaces is a power of 2 |✓|||| 
| **Routing** | Static routes |✓||||
| **IPv6** |  Static routes |✓||||
| **Load balancing** |  Single Listener Address |✓||||
||Servers - BIG-IP System (Single)  |✓||||
||Servers - BIG-IP System (Redundant pair)  |✓||||
||Virtual Servers - Manual Configuration  |✓||||
||Wide IPs - Standard FQDN Names  |✓||||
||Wide IPs - Standard FQDN Alias Names  |✓||||
||Wide IPs - Single Pool, Multiple Virtual Server Members |✓||||
||Algorithms - Static - Round Robin, Ratio (Weighted Round Robin), Global Availability  |✓||||
||Algorithms - Dynamic - Least Connections  |✓||||
| **DNS** | Authoritative Name Server for Specific Subdelegated Domains |✓||||
| **Management** |  Buffered Logging  |✓||||
||Log shipping to log correlation device (Within customer's account)  |✓||||
| **High availability (HA)** |  Synchronization Groups  |✓||||
||Redundant GTM Devices specified as primary and secondary DNS servers  |✓||||
| **Modes and modules** | Serial configuration  |✓||||
||Paralled configuration  |✓||||
||Standalone BigIP with GTM License |✓||||


### Cisco CSS
End of support on September 30, 2014. Customers that continue using the platform will be in the Extended Lifecycle Support. All the support will be Reasonable endeavor.

### Redhill WebMux
End of support. Customers that continue using the platform will be in the Extended Lifecycle Support . All the support will be Reasonable endeavor.

### General topics
| Feature | Support level | 
| :--- |:--- |
| DDoS mitigation | Supported|
