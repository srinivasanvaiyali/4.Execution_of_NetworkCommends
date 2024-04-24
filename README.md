# Develop By:SRINIVASAN.V
# Reg No:212222043008
# 4.Execution_of_NetworkCommands
## AIM :Use of Network commands in Real Time environment
## Software : Command Prompt And Network Protocol Analyzer
## Procedure: To do this EXPERIMENT- follows these steps:
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer. All commands related to Network configuration which includes how to switch to privilege mode and normal mode and how to configure router interface and how to save this configuration to flash memory or permanent memory. This commands includes • Configuring the Router commands • General Commands to configure network • Privileged Mode commands of a router • Router Processes & Statistics • IP Commands • Other IP Commands e.g. show ip route etc.

## Program
## client program
import socket  
from pythonping import ping   
s = socket.socket()   
s.bind(('localhost', 8000))   
s.listen(5)   
while True:   
c, addr = s.accept()   
print("Connection from", addr)   
try:   
hostname = c.recv(1024).decode().strip()   
if hostname:   
try:   
response = str(ping(hostname, verbose=False))   
c.send(response.encode())   
except Exception as e:   
c.send("Ping failed: {}".format(e).encode())    
else:   
c.send("Hostname not provided".encode())   
except Exception as e:   
print("Error:", e)   
finally:   
c.close()   

server   
import socket s = socket.socket()   
s.connect(('localhost', 8000))   
try:   
while True:   
ip = input("Enter the website you want to ping: ")   
s.send(ip.encode())   
response = s.recv(1024).decode()  
if response:   
print("Ping Result:", response)   
else:   
print("No response from server.")   
except Exception as e:   
print("Error:", e)  
finally:  
s.close()   


In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer
All commands related to Network configuration which includes how to switch to privilege mode
and normal mode and how to configure router interface and how to save this configuration to
flash memory or permanent memory.
This commands includes
• Configuring the Router commands
• General Commands to configure network
• Privileged Mode commands of a router
• Router Processes & Statistics
• IP Commands
• Other IP Commands e.g. show ip route etc.
## TRACECODE COMMAND :
from scapy.all import *   
target = ["www.google.com"]   
result, unans = traceroute(target,maxttl=32)  
print(result,unans)   
<BR>
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
<BR>
All commands related to Network configuration which includes how to switch to privilege mode
<BR>
and normal mode and how to configure router interface and how to save this configuration to
<BR>
flash memory or permanent memory.
<BR>
This commands includes
<BR>
• Configuring the Router commands
<BR>
• General Commands to configure network
<BR>
• Privileged Mode commands of a router 
<BR>
• Router Processes & Statistics
<BR>
• IP Commands
<BR>
• Other IP Commands e.g. show ip route etc.
<BR>

## Output
## Client & Server
![image](https://github.com/srinivasanvaiyali/4.Execution_of_NetworkCommends/assets/145117665/2988644b-29c1-476f-898a-df7df5f3df3d)
## TRACECODE COMMAND
![image](https://github.com/srinivasanvaiyali/4.Execution_of_NetworkCommends/assets/145117665/b3f88f07-745b-4ac8-94e3-d3c906518a42)


## Result
Thus Execution of Network commands Performed 
