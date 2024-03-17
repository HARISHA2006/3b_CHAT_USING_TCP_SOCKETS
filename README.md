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
CLIENT
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
   msg=input("Client > ") 
   s.send(msg.encode()) 
   print("Server > ",s.recv(1024).decode())
```
SERVER
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
## OUTPUT
CLIENT:

![Screenshot 2024-03-17 212425](https://github.com/HARISHA2006/3b_CHAT_USING_TCP_SOCKETS/assets/148843830/883e6b0a-8730-4770-bf03-a4a39fa43157)

SERVER:

![Screenshot 2024-03-17 212419](https://github.com/HARISHA2006/3b_CHAT_USING_TCP_SOCKETS/assets/148843830/ff450e3e-85a0-4687-b2bf-52d10910f7ac)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
