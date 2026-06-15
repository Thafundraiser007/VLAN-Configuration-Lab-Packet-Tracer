# VLAN-Configuration-Lab-Packet-Tracer
This lab demonstrates the creation and configuration of Virtual Local Area Networks (VLANs) on a Cisco switch using Cisco Packet Tracer. VLANs were created and switch ports were assigned to the appropriate VLANs. The configuration was then verified using the show vlan brief command.

Objectives:
-Create VLANs on a Cisco switch.
-Assign switch ports to specific VLANs.
-Verify VLAN configuration using Cisco IOS commands.

Devices Used:
-Cisco 2960 Switch
-Cisco Packet Tracer

VLAN Config:
| VLAN ID | Department |
| ------- | ---------- |
| 10      | ICT        |
| 20      | HR         |
| 30      | Finance    |

Port Assignment
| Port  | VLAN    | Department |
| ----- | ------- | ---------- |
| Fa0/1 | VLAN 10 | ICT        |
| Fa0/2 | VLAN 20 | HR         |
| Fa0/3 | VLAN 30 | Finance    |

Config Commands:
-Create Vlan
enable
configure terminal
vlan 10
name ICT
vlan 20
name HR
vlan 30
name Finance
end

-Port Assignment
configure terminal
interface fa0/1
switchport mode access
switchport access vlan 10
interface fa0/2
switchport mode access
switchport access vlan 20
interface fa0/3
switchport mode access
switchport access vlan 30
end

Verification:
show vlan brief

Expected Output:
VLAN Name                             Status    Ports
---- -------------------------------- --------- --------------------------
1    default                          active
10   ICT                              active    Fa0/1
20   HR                               active    Fa0/2
30   Finance                          active    Fa0/3

Skills Demonstrated:
-VLAN creation and naming
-Individual port VLAN assignment
-Switch configuration using Cisco IOS
-VLAN verification using show vlan brief

Files Included:
-VLAN-Lab.pkt
-README.md
-Screenshots

Author
Jamill Naipao
