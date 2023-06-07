# CREATION-FOR-ECHO-CLIENT-AND-ECHO-SERVER-USING-TCP-SOCKETS
CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS

EXP: 8

DATE:  24/04/2023

AIM:

To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.

ALGORITHM:

1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server, it will send ACK signal to client otherwise it will
send NACKsignal to client.
6. Stop the program


PROGRAM:

CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
 ```
SERVER:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
 ```
OUTPUT:

CLIENT:

![5client](https://github.com/MaheshMuthuL/CREATION-FOR-ECHO-CLIENT-AND-ECHO-SERVER-USING-TCP-SOCKETS/assets/135570619/4df0136b-a680-453b-90ac-47d33d661ae7)






SERVER:

![5server](https://github.com/MaheshMuthuL/CREATION-FOR-ECHO-CLIENT-AND-ECHO-SERVER-USING-TCP-SOCKETS/assets/135570619/9d992ebc-c693-459b-84a0-ba0a74a59131)






RESULT:

Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links
was successfully created and executed.
