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
## server.py:

import socket
HOST , PORT = '127.0.0.1',65432
with socket.create_server((HOST,PORT)) as s:
    conn, addr = s.accept()
    with conn:
        print(f'connected by {addr}')
        while data := conn.recv(1024):
            conn.sendall(data)

## client.py:

import socket
HOST, PORT = '127.0.0.1',65432
with socket.create_connection((HOST, PORT)) as s:
    s.sendall(b'hari ,212223040059')
    print(f'Received: {s.recv(1024)!r}')


## OUTPUT:
## server.py:
![image](https://github.com/user-attachments/assets/4fc36e6d-78ef-428c-a18c-05b765aef98d)

## client.py:
![WhatsApp Image 2025-03-03 at 14 25 15_7dbcfdd2](https://github.com/user-attachments/assets/0b5a2a52-1a12-4ee8-99a1-b7d037ebecf5)

## RESULT:
The program is executed successfully
