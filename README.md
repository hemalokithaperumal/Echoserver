# Echoserver
Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:

# Client.py
```
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_connection((HOST, PORT)) as s:
    s.sendall(b'HEMALOKITHA PERUMAL, 212223110014')
    print(f'Received: {s.recv(1024)!r}')
```
# Server.py
```
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_server((HOST, PORT)) as s:
    conn, addr = s.accept()
    with conn:
        print(f'Connected by {addr}')
        while data := conn.recv(1024):
            conn.sendall(data)
```
## OUTPUT:
![image](https://github.com/user-attachments/assets/a1423e2a-62c7-43fb-874b-b61e70909889)

## RESULT:
The program is executed successfully.
