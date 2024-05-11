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
### Client
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
   msg=input("Client > ") 
   s.send(msg.encode()) 
   print("Server > ",s.recv(1024).decode())
```
### Server
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
### CLient
![323145564-859c9047-79f8-4173-8415-7e09c238c26a](https://github.com/s-adhithya/3b_CHAT_USING_TCP_SOCKETS/assets/113497423/64b977c5-c0aa-42fd-b713-969ac1960fd4)

### Server
![323145617-7c2d13ce-8eb7-48b6-9e5f-77b3d0f920ad](https://github.com/s-adhithya/3b_CHAT_USING_TCP_SOCKETS/assets/113497423/9a25a5c5-6b15-42e5-93e6-eb783a623ac4)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
