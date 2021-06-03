# Zabbix-IBM-v3500-v7000-template
Use for monitoring of IBM v3500, v3700 and v7000 storage systems within Zabbix.

Supports multiple enclosures and monitors power supplies, vdisks, arrays, canisters and disks.

Adapted from the original script created by Francisco Tudel 2015

To use simply:
* copy the v3700_status.sh file to /usr/lib/zabbix folder on your zabbix server.
* Import the template file into your templates section within the Zabbix ui.
* Create a new user on your storage system which Zabbix can use.
* Then create your host as per mornal but adding the following user macros:
* {$CABIP1} - this is the IP address of your storage system
* {$CABPASS} - Password of your new user
* {$CABUSER} - Username of your new user

Then execute the 4 discovery rules, which should then populate all the items you need for monitoring.
