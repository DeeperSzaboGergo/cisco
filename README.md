# cisco
hostname s3
ip dhcp excluded-address:inentől-idáig zár ki
enable password ena12345
line con 0	
password con12345
login
exit
ip domain name m013.local
crypto key generate rsa
1024
line vty 0 15
transport input ssh
exit
username sshadmin privilege 15 secret ssh12345
service password-encryption
interface vlan 1
ip address 192.168.1.203 255.255.255.0
no shutdown
exit

amelyik interface-be megy oda:
(sw interface)(swichek közöt)swichport mode trunk
swichport mode access
swichport access vlan 20(amelyik vlanon van)
Levédések
interface range fa0/5-24(amit le szeretnék kapcsolni)
shutdown
statikus ip irányítás:
ip route (a cél ip+mask) következő ugrási pont interface (fa0/1,se0/1/0)
show ip rout mi kell igazábol 
serial dte:adunk órajelet, dce:nem adunk órajelet
no clock rate
channel-group 1 mode activate 2kábelt összefog
befogadó kábel ip helper-address cél ip:server dhcp




