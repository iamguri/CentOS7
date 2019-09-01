
#### In this we are going to see that how we can configure openSSL ie HTTPS on our local webserver and secure our website with https protocol.

### What is openSSL?

### openSSL is general purpose cryptography library that provides an open source implementation of SSL(Secure Socket Layer) and TLS(Transport Layer Security) 

### Packages that we need to install before configuration.
### httpd*, mod-ssl*

### [root@Desktop]# openssl req -x509 -days 365 newkey rsa:2048 -nodes -keyout /etc/pki/tls/private/key.key -out /etc/pki/tls/certs/key.crt


Where: <br />

+ req -x509 : 509 certificate signin request <br />
+ days 365  : validity in days<br/ >
+ newkey    : creation of new key <br />
+ rsa:2048  : encrypting with 2048 (you can use 3072, 4096 etc)<br />
+ keyout    : for key <br />
+ out       : for certificate <br />
+ nodes     : to skip the option of securing certificate with paraphrase (i.e. to skip asking password again and again)<br />


How to configure website on local machine?
[Visit Here](https://github.com/iamguri/CentOS7/blob/master/LocalWebServer/LocalWebServer_Script "Local Web Server")
