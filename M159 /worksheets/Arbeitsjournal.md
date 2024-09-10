Kerberos Realm: Domain, über die Kerberos die Berechtigung hat user zu Services zu authentifizieren. Realms können verbunden werden

In einem Realm gibt es Prinicipals (User, Services), unique.

![grafik](https://github.com/user-attachments/assets/e71f58f0-10a8-49bc-aa18-277012cf0e52)


KDC supplies Tickets, generates temporary Session keys, that allows user to authenticate to a service. The KDC stores the secret symetric keys for users and services. 

    In the KDC are 2 Servers: Authen. Server, Ticket Granting Server.
    The Auth. Server confirms and issues TGT. TGS confirms that a user is making a request to a known service. Issues Service Ticket

Messages:

- Authenticators: allow the users authenticate to the service, and the services authenticate to the server.
- Tickets: Contain most information, clients identify, service key, session key, timestamp, TTL (encrypted, using servers secret key)

Communication for a user gaining access to a service:

1. User to auth. Server. Auth. Server validates with TGT

2. TGT back to user, encrypted with secret key. User decrypts the message with secret key

3. user creates new messages and sends with TGT to the Ticket Granting Server

4. Ticket Granting Service decrypts the TGT, generates a service ticket. It gets send back to the user

5. User decrypts message, creates a auth. message and sends the auth. message with the TGT to the Service

6. Service creates own final auth. message is send back to the user.

-> distribute a symmetric service session key. Communication

![grafik](https://github.com/user-attachments/assets/f1bfed5e-1a51-4bf7-84c7-acde06e1a4e8)

Key Distro Center

