
In this we are going to see that how we can configure openSSL ie HTTPS on our local webserver

What is openSSL?
openSSL is general purpose cryptography library that provides an open source implementation of SSL(Secure Socket Layer) and TLS(Transport Layer Security) 

+ Packages that we need to install before configuration.
- httpd*, mod-ssl*

[root@Desktop]# openssl req -x509 -days 365 newkey rsa:2048 -nodes -keyout /etc/pki/tls/private/key.key -out /etc/pki/tls/certs/key.crt

Where:

req -x509 : 509 certificate signin request
days 365  : validity in days
newkey    : creation of new key 
rsa:2048  : encrypting with 2048 (you can use 3072, 4096 etc).
keyout    : for key
out       : for certificate
nodes     : to skip the option of securing certificate with paraphrase (to skip asking password again and again generally).


How to configure website on local machine?
follow this : [visit here] https://github.com/iamguri/CentOS7/blob/master/LocalWebServer/LocalWebServer_Script ("Local Web Server")
