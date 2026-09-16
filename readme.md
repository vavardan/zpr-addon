# **[OCI ZRP Addon for Operating Entities Landing Zone](#)**

&nbsp; 

## **Overview**
This addon integrates OCI **Zero Trust Packet Routing (ZPR)** into the One-OE Landing Zone as an additional network security and governance layer.

The One-OE Landing Zone already uses multiple controls to secure network communication, including **routing, Security Lists, Network Security Groups (NSGs), and OCI Network Firewall**. These controls are primarily managed by the Network and Project administration teams.

The ZPR addon complements these existing controls by introducing an independent, **attribute-based policy layer** managed by the Security administration team. This enables the Security team to enforce organization-wide security and compliance requirements without depending on, or replacing, the underlying network configuration.

A key objective of this addon is to provide a clear separation of responsibilities between the **Network**, **Project**, and **Security** teams:

- **Network** and **Project** teams manage network connectivity and traditional network security controls.

- **Security** teams define and govern ZPR Namespaces, Security Attributes and ZPR Policies that determine which protected endpoints are allowed to communicate.

For communication between two endpoints to succeed, all applicable network security controls must allow the traffic. **A permissive rule in one layer does not override a more restrictive rule in another layer.**

&nbsp;

The animations below illustrate this multi-layer enforcement model.

**First use case - communication allowed:**
The Security team allows communication between the two endpoints through ZPR, while routing, Security Lists or NSGs, and OCI Network Firewall also permit the traffic. Because all applicable controls allow the communication- a logical AND, the destination endpoint can be reached.

&nbsp;
<img src="./zpr_allow.gif" width="900" height="value">

&nbsp;

**Second use case - communication blocked:**
Routing, Security Lists or NSGs, and OCI Network Firewall allow the traffic, but the Security team does not permit the communication through ZPR policies. Because all applicable controls must allow the traffic, the communication is blocked and the destination endpoint cannot be reached.

&nbsp;
<img src="./zpr_block.gif" width="900" height="value">

&nbsp;

&nbsp;

&nbsp;


  
&nbsp;


&nbsp;

&nbsp;




&nbsp;

> [!NOTE]


&nbsp;

#### Summary

&nbsp;

### Configuration and deployment

&nbsp; 

#### License
Copyright (c) 2026 Oracle and/or its affiliates.

Licensed under the Universal Permissive License (UPL), Version 1.0.

See [LICENSE](/LICENSE.txt) for more details.