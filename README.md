# 4.Execution_of_NetworkCommands
## AIM :Use of Network commands in Real Time environment
## Software : Command Prompt And Network Protocol Analyzer
## Procedure: To do this EXPERIMENT- follows these steps:
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
##PROGRAM:
DEVELOPED BY:ATCHAYA.K


REGISTER NUM:212223220011
##PING COMMAND
CLIENT:
```
import socket 
from pythonping import ping 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    hostname=c.recv(1024).decode() 
    try: 
        c.send(str(ping(hostname, verbose=False)).encode()) 
    except KeyError: 
        c.send("Not Found".encode())
```
SERVER:
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    ip=input("Enter the website you want to ping ") 
    s.send(ip.encode()) 
    print(s.recv(1024).decode())
```
TRANSCEROUTE COMMAND:
```
from scapy.all import* 
target = ["www.google.com"] 
result, unans = traceroute(target,maxttl=32) 
print(result,unans)
```

## Output
##PING COMMAND
CLIENT:
![image](https://github.com/Atchayakunchithapatham/4.Execution_of_NetworkCommends/assets/144870744/9a9b782f-6fbe-47a8-8991-4d1faa347360)
SERVER:
![image](https://github.com/Atchayakunchithapatham/4.Execution_of_NetworkCommends/assets/144870744/5f180fa6-5783-46ed-91fc-633d625dd397)
TRANSCEROUTE COMMAND:
![image](https://github.com/Atchayakunchithapatham/4.Execution_of_NetworkCommends/assets/144870744/9db3f008-8074-4f7f-88c3-9fb99b442390)



## Result
Thus Execution of Network commands Performed 
