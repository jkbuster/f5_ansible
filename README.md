NOTE:  All certificates and hostnames in this repo are fictional

Creating a new certificate:
1. create site directory
2. Create openssl.cnf file
3. in the directory, run the following command to generate a new key and CSR:
openssl req -config openssl.cnf -new -out csr.pem
4. Verify the CSR with the following command:
openssl req -noout -text -in csr.pem
5. Send the CSR to your CA for signing
6. Once it's signed, place it in the site's directory as cert.pem
7. Place the CA's intermediate bundle in the site's diretory as bundle.pem

Distributing Certificates:

