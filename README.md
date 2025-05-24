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

## Program:
## Client:
```
 import socket 
from pythonping import ping 
s=socket.socket() 
s.bind(('localhost'8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
   hostname=c.recv(1024).decode() 
   try: 
       c.send(str(ping(hostname, verbose=False)).encode()) 
   except KeyError: 
       c.send("Not Found".encode())
```
## Server:
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    ip=input("Enter the website you want to ping ") 
    s.send(ip.encode()) 
    print(s.recv(1024).decode())
```

## Output

## IPCONFIG:
![444850105-dcda3df7-a259-41b9-ac59-1277209d4b58](https://github.com/user-attachments/assets/7730fcdb-b9ad-433c-971a-8a5142253b65)
## PING:
![444850297-dd2924d1-ad49-45fb-b663-bb9dd5f12eae](https://github.com/user-attachments/assets/4c0bba9e-141e-4039-b4f2-e4366a98889f)
## ARP:
![444850878-65186445-533e-49e7-b9aa-3423525a4dab](https://github.com/user-attachments/assets/a4dcf6b6-6956-4d6a-98bc-cc5450b34ece)
## NETSTAT:
![444851266-51c33d42-cef7-42c0-a1e8-6b2cf1eb0cb4](https://github.com/user-attachments/assets/105a1fe6-ac90-47b3-923f-0cec2cfa0af3)
![444851639-a6f446ae-013a-48ef-a455-6a162b8249ef](https://github.com/user-attachments/assets/cd85a35e-de55-414c-94e6-4b54e1a0f20d)
![444851813-e4d505b1-3e4f-4aa4-a3cd-dc6941999bb3](https://github.com/user-attachments/assets/49cbf84a-7e8f-44a7-ab16-f3e192d38888)
![444851993-d0baa96d-bc29-49ca-ad98-d511a26d079d](https://github.com/user-attachments/assets/6b85e983-72dd-4ff4-9dd1-05bf5f0e7632)

## Result
Thus Execution of Network commands Performed 
