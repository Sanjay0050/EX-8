# EX-8 APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER

## DATE:26-04-2023
## AIM:

To write a python program for creating Echo Client and Echo Server using TCP Sockets Links.
## ALGORITHM:

Import the necessary modules in python Create a socket connection to using the socket module. Send message to the client and receive the message from the client using the Socket module in server. Send and receive the message using the send function in socket.
## PROGRAM:
## CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
   msg=input("Client > ")
   s.send(msg.encode())
   print("Server > ",s.recv(1024).decode())
```
## SERVER:
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
## CLIENT OUTPUT :

![241142551-70336953-f1c4-4c6b-bb75-5a2c591ff153](https://github.com/Amruthavarshnibs/EX-8/assets/119103704/5a7165e4-137e-443e-931c-5f78abf62c41)

## SERVER OUTPUT :

![241142582-c1ad24b0-f5a8-4eb7-92f8-fd35df70dc76](https://github.com/Amruthavarshnibs/EX-8/assets/119103704/33fe6a17-cad1-42b6-ab11-312175d957df)

## RESULT:

Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.
