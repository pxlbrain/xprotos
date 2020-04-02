**SSL:**

Generated on AWS using certificate manager.

1. Export certs.
2. Decrypt private key using passphrase, for example:
- openssl rsa -in private_key.pem -out decrypted_private_key.pem
3. Convert private key to support netty requirements (https://netty.io/wiki/sslcontextbuilder-and-private-key.html)
- openssl pkcs8 -topk8 -nocrypt -in decrypted_private_key.pem -out pkcs8_key.pem
4. Rename Certificate.txt to cert.pem and private key to key.pem
5. Copy keys

Latest key is wildcard key:
 - *.pixlops.com
