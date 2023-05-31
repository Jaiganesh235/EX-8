# EX-8 APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER

# DATE : 26-04-2023

## AIM :
To write a python program for creating Echo Client and Echo Server using TCP Sockets Links.


## ALGORITHM :
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in server.
4. Send and receive the message using the send function in socket.

## PROGRAM :
### CLIENT :
```
# Developed by: S,JAIGANESH
# Register No: 212222240037
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
``` 
### SERVER :
```
# Developed by: S.JAIGANESH
# Register No: 212222240037
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
``` 

## OUTPUT :
### CLIENT:
![Screenshot (109)](https://github.com/Jaiganesh235/EX-8/assets/118657189/bba6fbb7-be41-41f6-812a-8e9a502332e7)

### SERVER:
![Screenshot (110)](https://github.com/Jaiganesh235/EX-8/assets/118657189/15a1d7ad-d217-4f5b-ad7d-9a035e46f677)


## RESULT :
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.
