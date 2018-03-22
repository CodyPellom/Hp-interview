Why SSL certificates Exist:

Encryption{Hiding what is sent from one computer to another. It's like speaking in code.

Why Encrypt? Any computer could hypothetically intercept information coming from HP servers to client's computers or vice versa. With encryption, if that information is intercepted, it is coded and the encrypted information is garbage: completely unusable. 
***************************************************
How does Encryption Work? There are five steps to put simply:
1. Computers agree on how to encrypt:
We have Server Computer (A) and Client Computer (B). (B) sends a message to (A) to agree on how to communicate w/ each other. The message contains

1. a Hash, which contains something called the "Message Authentication Code". This is used to verify the intergrity of the exchange.

2. a Cipher, which is the method or way of encrypting the messages between the two servers.

3. and the Key Exchange Method, which can be RSA, Diffie-Hellman, DSA etc. 

4. Version of SSL is also sent, indicating TLS

5. and a random number which is used to compute the master secret which is used from then on to calculate the encryption keys. 

Once the client sends the "hello" message to the server, the server will then respond with a message which contains the Key, Cipher and Hash to be used in order to communicate securely. Once agreed, they are ready to move on to the next step.

Next, the server sends a certificate to the client. The certificate contains information on who the server belongs to, how long the certificate is valid for, various serial numbers and more importantly: the public key. 
    Next the client computer sends a message which says effectively "Let's Start Encrypting" 



2. Server sends a certificate
3. YOur computer says 'start encrypting'
4. The server says 'Start encrypting'
5. ALL messages are now encrypted}
***************************************************

Identification{ How can you trust what computer is on the other end? through Identification}