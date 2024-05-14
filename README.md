# 3b.CREATION FOR CHAT USING TCP SOCKETS
### NAME: LOKESH RAHUL V V
### REG NO:212222100024
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
### CLIENT:
```python
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
   msg=input("Client > ") 
   s.send(msg.encode()) 
   print("Server > ",s.recv(1024).decode())
```
### SERVER:
```python
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
### client
![image](https://github.com/lokeshrahulv/3b_CHAT_USING_TCP_SOCKETS/assets/118423842/310860f0-ec3c-4f1a-b4a8-31eb62b3b324)
### server
![Screenshot 2024-05-14 143545](https://github.com/lokeshrahulv/3b_CHAT_USING_TCP_SOCKETS/assets/118423842/eac21cb6-5960-462f-834d-2bbda92ed3f9)
## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
