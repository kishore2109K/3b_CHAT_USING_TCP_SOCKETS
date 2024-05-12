# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.

# NAME : KISHORE K
# REGISTER NAME : 212223040101
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM:
## client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## server:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())
```
## OUTPUT:
## client:
![image](https://github.com/kishore2109K/3b_CHAT_USING_TCP_SOCKETS/assets/152274619/ccaa11f1-6cda-4700-b18f-f0e0d1a89971)

## server:
![image](https://github.com/kishore2109K/3b_CHAT_USING_TCP_SOCKETS/assets/152274619/946f00dd-74d7-48df-bf6a-930f323302ff)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
