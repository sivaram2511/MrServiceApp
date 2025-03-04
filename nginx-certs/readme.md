create folder for nginx certificates
mkdir ~/nginx-certs
cd ~/nginx-certs

create self-signed certificate
openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout nginx-selfsigned.key -out nginx-selfsigned.crt