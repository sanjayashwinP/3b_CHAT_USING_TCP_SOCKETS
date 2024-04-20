# 3b.CREATION FOR CHAT USING TCP SOCKETS
### NAME:SANJAY ASHWIN P    
### REG NO:212223040181
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## CLIENT
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## SERVER
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
## OUPUT
## CLIENT
![Screenshot 2024-04-20 110511](https://github.com/sanjayashwinP/3b_CHAT_USING_TCP_SOCKETS/assets/147473265/9ccc35f9-c99e-4e1a-9f82-e9727fbb2cfc)

## SERVER
![Screenshot 2024-04-20 110532](https://github.com/sanjayashwinP/3b_CHAT_USING_TCP_SOCKETS/assets/147473265/afebfbdf-5395-4538-8a57-3695c437148f)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
