# 2a_Stop_and_Wait_Protocol
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM

```
NAME : KAVIYA D

REGISTER NUMBER : 212223040089
```
## CLIENT:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
   i=input("Enter a data: ")
   c.send(i.encode())
   ack=c.recv(1024).decode()
   if ack:
     print(ack)
     continue
   else:
     c.close()
     break
```
## SERVER:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    print(s.recv(1024).decode())
    s.send("Acknowledgement Recieved".encode())
```
## OUTPUT

## CLIENT:
![322496676-285f80ef-2e8d-41a6-b734-0fb4f35e819e](https://github.com/user-attachments/assets/b0605213-3742-4a97-b02d-c74e0cbd9e5f)

## SERVER:
![322496812-ca3a1f95-8af3-4ac3-9768-0609e6ece1a4](https://github.com/user-attachments/assets/9d53700b-7beb-4204-96cb-8fb3353190e6)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
