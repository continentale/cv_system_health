# cv_system_health

A php based nagios / icinga / naemon compliant health check for various snmp devices. The main goal of this project aims to be easily extendable by adding simple xml files to the check in order to check new hardware,  therefore contributions are welcome. The check supports SNMPv3 (currently only authPriv is supported), SNMPv2c and SNMPv1. 

It is possible to add custom MIB files to the Vendor/Mibs folder in order to use Short OID names, however the numeric OID is prefered due to performance reasons.


### system requirements
- php5 / php7 with mod_snmp, mod_xml enabled

### Usage examples

##### SNMPV1
``` ./cv_system_health -h=10.10.0.1 -C=public -v1```

##### SNMP V2
``` ./cv_system_health -h=10.10.0.1 -C=public ```

##### SNMP V3
``` ./cv_system_health -h=10.10.0.1 -u=snmpusername -p=password -e=SHA -E=AES ```


##### SNMP V3 with custom xml file to load
``` ./cv_system_health -h=10.10.0.1 -u=snmpusername -p=password -e=SHA -E=AES --xml=msycustom.xml ```

### supperted systems / devices
there are various devices supported such as

##### Server Management Boards
Fujitsu iRMC S4 & S5, Dell iDRac V8 and V9, HP ILO4,  Lenovo IMM2

##### PDU
Raritan PDU, Raritan PDU2

##### Firewalls 
Cisco ASA, Uniper MX5

##### Telephony systems
Unify Hipath 4000, Unify OpenScape V9

##### Switches  / Routing Switches
 Extreme Networks VSP, Nexans GigaSwitch, Microsens MicroSwitch

##### fiber channel multiplexer
PanDaCom Multiplexer with various modules

##### Video Conferencing 
PolyCom Real Presence Access Director

##### Storage Systems
EMC Isilon Cluster (CLuster and Sigle nodes)