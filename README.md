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

NAME: JAYASHREE J
REGISTER NUMBER: 212225040145

CLIENT:
import socket 
s=socket.socket() 
s.connect(('localhost',9000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())

SERVER:
import socket 
s=socket.socket() 
s.bind(('localhost',9000)) 
s.listen(5) 
c,addr=s.accept()
while True: 
    ClientMessage=c.recv(1024).decode() 
    print("Client > ",ClientMessage) 
    msg=input("Server > ") 
    c.send(msg.encode())
    
## OUPUT

CLIENT:

<img width="1600" height="899" alt="image" src="https://github.com/user-attachments/assets/5fbbd8c1-e730-4190-b95b-7453711e8ae0" />

SERVER:

<img width="1600" height="896" alt="image" src="https://github.com/user-attachments/assets/cfe6b7e3-2fea-457f-8ebc-a8ef5dad7add" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
