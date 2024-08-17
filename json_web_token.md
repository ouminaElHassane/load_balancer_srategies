JWT Explained 

JWT, or JSON Web Token, is an open standard (RFC 7519) that defines a compact way to securely transmit information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs are commonly used for authentication and information exchange in web applications.

Structure of a JWT
A JWT is divided into three parts, separated by dots (.):

# 1-Header:
The header typically consists of two parts: the type of the token, which is JWT, and the signing algorithm being used, such as HMAC SHA256 or RSA.

# 2-Payload:
The payload contains the claims (statements about an entity: typically, the user, and additional data). Claims are divided into three categories:
Registered claims: Standardized claims that are not mandatory but recommended, such as iss (issuer), exp (expiration time), sub (subject), aud (audience), etc.
Public claims: Custom claims created by the user to share information. They should be defined in the IANA JSON Web Token Registry or be collision-resistant to ensure uniqueness.
Private claims: Custom claims created to share information between parties that agree on its usage.

# 3-Signature:
To create the signature part, you take the encoded header, the encoded payload, a secret (or private key), and the algorithm specified in the header. The resulting signature ensures that the token hasn’t been altered and verifies the sender.

Use Cases of JWT
# 1-Authentication:
After a user logs in, a JWT can be generated and sent to the client. The client stores this token (usually in local storage) and sends it along with each request to access protected routes. The server can verify the token and authorize the user without needing to query the database every time.

# 2-Information Exchange:
JWTs can be used to transmit claims or data securely between parties. Since it is signed, the receiver can trust that the data was sent by the expected sender.

Advantages of JWT
Compact: JWTs are compact and can be sent via URL, POST parameters, or inside HTTP headers.
Self-contained: They contain all the necessary information about the user or the session, which means no extra database lookup is necessary.
Secure: They allow for various signing algorithms, and you can also encrypt the contents to ensure confidentiality.

Security Considerations
Secret Management: Keep your signing keys secret. Exposure of these keys can lead to token forgery.
Token Expiration: Always set an expiration time for your JWTs to limit the risk of token theft.
Storage: Store tokens securely (consider using HttpOnly and Secure cookies to mitigate XSS attacks).
![1722871696115](https://github.com/user-attachments/assets/f9e13f1b-4c40-44b6-91aa-07897659a180)
