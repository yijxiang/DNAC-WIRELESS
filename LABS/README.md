# DNAC-WIRELESS LABS 
## Overview
This section is built out in LAB form to guide you through the typical steps required to enable the various automation tasks delivered by DNA Center specific to the wireless environment. This lab will give examples of how to automate the wireless equipment via DNA Center. The intention is to give examples that can be modified for your use and tested on equipment within the dCLOUD LAB environment. Additional information within the lab provides a well-rounded explanation of Automation methods. Lastly, the lab allows for customers to use DNA Center workflows to practice deploying Onboarding, Building a Cisco Unified Wireless Network, utilizing Application Policy automation across Cisco Wireless Platforms.

The goal of this lab is for it to be a practical guide to aid engineers to rapidly begin using DNA Center automation and help them work towards an adoption strategy. Additionally, this lab will give customers a permanent place to try out wireless automation and include configurations for various use cases. This environment will enable engineers to reduce the time and effort needed to instantiate the network.

As a result, customers will gain experience setting up Plug and Play ,onboarding and configuring Cisco wireless. Additionally, they will use templating and troubleshooting tools, which may help during faultfinding to determine what is failing in a deployment.

## Labs
Please use this menu to navigate the various sections of this Github repository. Within the multiple folders are examples, explanation readme files for reference.

* [PnP Preparation](https://github.com/kebaldwi/DNAC-WIRELESS/blob/master/LABS/LAB1-PNP-PREP/) - This lab explains the overall Global Plug and Play set up steps
* [Controller PnP](https://github.com/kebaldwi/DNAC-WIRELESS/blob/master/LABS/LAB2-Pnp-Discovery/) - This lab explains in depth and how to use Plug and Play with a Cisco 9800 Controller
* [Controller HA](https://github.com/kebaldwi/DNAC-WIRELESS/blob/master/LABS/LAB3-Controller-HA/) - This lab will dive into Controller High Availability
* [WLANs](https://github.com/kebaldwi/DNAC-WIRELESS/blob/master/LABS/LAB4-WLANs/) - This lab will explore how to build Wireless LAN's
* [AP Provisioning](https://github.com/kebaldwi/DNAC-WIRELESS/blob/master/LABS/LAB5-AP-Provisioning/) - This lab will explore how to Onboard and Provison
* [Application Policys](https://github.com/kebaldwi/DNAC-WIRELESS/tree/master/LABS/LAB6-Application-Policy/) - This lab will explain Application Policys in DNAC and their use
* [Telemetry](https://github.com/kebaldwi/DNAC-WIRELESS/tree/master/LABS/LAB7-Telemetry-Enablement/) - This lab will explain how to deploy Telemetry for assurance
* [Advanced Automation](https://github.com/kebaldwi/DNAC-WIRELESS/tree/master/LABS/LAB8-Advanced-Automation/) - This lab will explore Advanced Automation examples 

## DCLOUD as a LAB
### Overview
This section will explain which lab to utilize within the **DCLOUD** environment to run these labs. It will also discuss a customer POC environment and the steps necessary to successfully run these sections within a customer environment for localized testing.

### DCLOUD Labs
This lab environment has been tested on the following DCLOUD session: [Cisco Enterprise Networks Hardware Sandbox v2.1](https://dcloud2-rtp.cisco.com/content/demo/759521?returnPathTitleKey=favourites-view)

The DCLOUD session includes the following equipment:

Virtual Machines:

    DNA Center 2.1.2.5
    Identity Services Engine (ISE) 3.0 (Not Configured)
    Stealthwatch 7.1
    FlowCollector 7.1
    Cisco Prime Infrastructure 3.9
    Wireless LAN Controller - C9800 running IOS-XE Amsterdam 17.3.3 code.
    Windows 10 Jump Host 
    Windows Server 2019 - Can be configured to provide identity, DHCP, DNS, etc.
    Windows 10 Clients 

Hardware Devices:

    ISR 4451 Router - 17.3.3 IOS-XE Code
    Catalyst 9300 Switch - 17.3.3 IOS-XE Code with Embedded Wireless Controller (EWC) and ThousandEyes Enterprise Agent
    Catalyst 3850 Switch - 16.12.5 IOS-XE Code
    4800 Access Points
    Silex Controller (2 NIC's)

The lab envionment that is available is depicted here:
![json](./LAB1-PNP-PREP/images/DCLOUD_Topology.png?raw=true "Import JSON")

## Disclaimer
Various labs are designed for use in the **DCLOUD** environment but can but are for use elsewhere. What is important to realize is the impact of each type of test. For instance, in the ***PnP Preparation*** lab, we go through discovery methods such as ***option 43*** and ***DNS Discovery***. If we were to use the DHCP option 43 and place that in the server options on the DHCP server, it would affect multiple scopes. **Care** is required, therefore, to ensure you do not get unexpected results. Similarly with ***DNS Discovery***, if the sub domain used was available to all devices, more than one device would discover DNA Center. Changes like this may be suitable for production in the future but detrimental during testing.

The environment allows for use with a web-based browser client for VPN-less connectivity, access as well as AnyConnect VPN client connectivity for those who prefer it. The labs are hosted out of our San Jose and RTP Facilities and so you would choose sessions from either US East or US West. Choose the Cisco Enterprise Network Sandbox v2.1 or 3.1. To access this or any other content, including demonstrations, labs, and training in Cloud please work with your Cisco Account team or Cisco Partner Account Team directly. Your Account teams will make sure the session is scheduled and shared for you to use. Once booked follow the guide within Github to complete the tasks adhering to the best practices of the dCLOUD environment.

If you found this set of Labs helpful please fill in comments and [give feedback](https://app.smartsheet.com/b/form/f75ce15c2053435283a025b1872257fe) on how we can improve.

