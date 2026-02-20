---
sidebar_position: 7
title: Our Lab
---

# Cybersecurity Lab

We are located in Vicki Lord Larson 1132 (between Schofield and the Library) where we have 4 racks of running equipment and two cabinets of other things. <!-- need better way to describe the things we have in our cabinets --> 

---

## Network Diagram

Outlined below is a flowchart representing the basic diagram of our in-lab network. A few things to note that aren't detailed in the flowchart are:

- The Netgear router is the only wireless access point in the system.
- The Linksys router acts as a barrier/firewall to create a "VLAN" within the UWEC network isolating the lab. This way, everything that happens in the lab, stays in the lab.
- Our CTF server is also isolated from the rest of the lab network using the Netgear router in a similar fashion.

```mermaid
flowchart LR;
    A@{ shape: cloud, label: "Internet" }-->uwec("UWEC Network");
    uwec --> linksys{"Linksys Router"};
    linksys l1@--> fog("FOG Server");
    linksys l2@--> netgear{"Netgear Router"};
    linksys l3@--> other("Other servers not managed by us yet");
    netgear --> ctf{{"CTF Server"}};
    l1@{ curve: linear }
    l2@{ curve: linear }
    l3@{ curve: linear }
```
 
