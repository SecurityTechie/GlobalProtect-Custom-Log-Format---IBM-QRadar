# Follow the below steps to configure custom log format for GlobalProtect Category logs in Palo Alto Firewall

Procedure 

1.  Log in to Palo Alto Networks.

2.  On the Device tab, click Server Profiles > Syslog, and then click Add.

3.  Create a Syslog destination by following these steps:

>   In the Syslog Server Profile dialog box, click Add.

>   Specify the name, server IP address, port, and facility of the QRadar system that you want to use as a Syslog server. 

>   If you are using Syslog, set the Custom Format column to Default for all log types.

4.  Configure LEEF events by following these steps:

>   Click the Custom Log Format tab in the Syslog Server Profile dialog.

>   Click GlobalProtect, copy the below log format and paste it in the GlobalProtect Log Format field for the GlobalProtect log type.

LEEF:2.0|Palo Alto Networks|PAN-OS Syslog Integration|$sender_sw_version|$action|x7C|ReceiveTime=$receive_time|SerialNumber=$serial|cat=$type|SubType=$subtype|GenerateTime=$time_generated|VirtualSystem=$vsys|EventID=$eventid|Stage=$stage|AuthenticationMethod=$auth_method|TunnelType=$tunnel_type|SourceUser=$srcuser|SourceRegion=$srcregion|MachineName=$machinename|PublicIP=$public_ip|PublicIPv6=$public_ipv6|PrivateIP=$private_ip|PrivateIPv6=$private_ipv6|HostID=$hostid|SerialNumber=$serialnumber|ClientVersion=$client_ver|ClientOS=$client_os|ClientOSVersion=$client_os_ver|RepeatCount=$repeatcnt|Reason=$reason|Error=$error|Description=$opaque|Status=$status|Location=$location|LoginDuration=$login_duration|ConnectMethod=$connect_method|ErrorCode=$error_code|Portal=$portal|SequenceNumber=$seqno|ActionFlags=$actionflags

5.  Click OK

6.  Click Commit.
