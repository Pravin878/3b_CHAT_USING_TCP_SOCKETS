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
s.bind(('localhost',9000))
s.listen(5)
c,addr=s.accept()
address={"6A:08:AA:C2":"192.168.1.100","8A:BC:E3:FA":"192.168.1.99"};
while True:
    ip=c.recv(1024).decode()
    try:
        c.send(address[ip].encode())
    except KeyError:
        c.send("Not Found".encode())
```
### Server
```
import socket
s=socket.socket()
s.connect(('localhost',9000))
while True:
    ip=input("Enter MAC Address : ")
    s.send(ip.encode())
    print("Logical Address",s.recv(1024).decode())
```
## OUPUT
### CLient
![Screenshot 2024-03-21 153833](https://github.com/s-adhithya/3b_CHAT_USING_TCP_SOCKETS/assets/113497423/871169ba-10c4-4660-adba-2731158c0ede)
### Server
![Screenshot 2024-03-21 153845](https://github.com/s-adhithya/3b_CHAT_USING_TCP_SOCKETS/assets/113497423/a62915d1-61c9-412a-bada-1eccc98bab8d)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
