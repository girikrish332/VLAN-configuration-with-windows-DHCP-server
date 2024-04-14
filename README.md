# Inter-VLAN Routing Configuration Guide

## Introduction

This guide provides step-by-step instructions for configuring inter-VLAN routing on a network device. Inter-VLAN routing allows communication between different VLANs within a network.

## Prerequisites

Before proceeding with the configuration, ensure you have the following:

- Access to the network device's management interface.
- Administrative access privileges.
- Basic understanding of VLANs and IP addressing.

## Configuration Steps

1. **Access the Device**: Ensure you have access to the network device through a console connection or SSH.

2. **Enter Configuration Mode**:
   - Enter privileged EXEC mode:
     ```
     enable
     ```
   - Enter global configuration mode:
     ```
     configure terminal
     ```

3. **Create VLANs (if not already created)**:
   If VLANs haven't been created yet, use the following commands for each VLAN:

vlan <vlan_id>
name <vlan_name>

vbnet


4. **Assign IP Addresses to VLAN Interfaces**:
For each VLAN, assign an IP address to its respective VLAN interface:

interface vlan <vlan_id>
ip address <ip_address> <subnet_mask>

markdown


5. **Enable Inter-VLAN Routing**:
Enable routing on the device:

ip routing

markdown


6. **Configure Inter-VLAN Routing**:
Create VLAN interfaces and assign them to their respective VLANs:

interface vlan <vlan_id>
ip address <ip_address> <subnet_mask>

markdown


7. **Verify Configuration**:
Verify the configuration using the following commands:

show vlan brief
show ip interface brief

markdown

Ensure that VLANs and their IP addresses are correctly configured.

8. **Save Configuration**:
Save the configuration to ensure changes persist after a reboot:

end
copy running-config startup-config

csharp


## Conclusion

Inter-VLAN routing is now configured on the network device, allowing communication between different VLANs within the network.

You can copy and paste this block of text into your preferred text editor or README.md file.
