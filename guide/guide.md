### Instructions 
#### How to get SSL certificate 
1. Certificate is under url http://mbeng_host:mbeng_port/cert<br/>
   You will download `.der` certificate. You should convert it to `.crt`
2. Convert certification <br/> 
    `sudo openssl x509 -inform der -outform pem -in local-ca.der -out local-ca.crt`<br/>
3. Installing a certificate in PEM form
   ```
   $ sudo apt-get install -y ca-certificates
   $ sudo cp local-ca.crt /usr/local/share/ca-certificates
   $ sudo update-ca-certificates
   ```