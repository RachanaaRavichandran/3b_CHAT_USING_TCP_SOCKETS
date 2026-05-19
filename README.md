# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
server.py
```
import socket

s = socket.socket()

s.bind(('localhost', 8000))

s.listen(5)

print("Waiting for client...")

c, addr = s.accept()

print("Connected with", addr)

while True:
    ClientMessage = c.recv(1024).decode()

    print("Client > ", ClientMessage)

    msg = input("Server > ")

    c.send(msg.encode())
```

client.py
```
import socket

s = socket.socket()

s.connect(('localhost', 8000))

while True:
    msg = input("Client > ")

    s.send(msg.encode())

    print("Server > ", s.recv(1024).decode())
devloped by:R.Rachanaa
ref no:212225040322

```

## OUPUT
server.py

<img width="461" height="250" alt="image" src="https://github.com/user-attachments/assets/8fe7cc25-5aa9-4289-8638-c111e807c30b" />

client.py

<img width="566" height="210" alt="image" src="https://github.com/user-attachments/assets/d1d3a5dd-3d97-401a-962a-aa440209d255" />


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
