# MrServiceApp
First .Net Core 3.1 App using docker

# use the docker file for spin up 3 server - https://localhost:3001, https://localhost:3002, https://localhost:3003
dokcer-compose up --build -d

# stop the servers
docker-compose down

# download the nginx server and replace nginx.conf, then it will acted as a reverse proxy for all 3 server
# https://localhost/

# How the SSL cert created
create folder for nginx certificates
mkdir ~/nginx-certs
cd ~/nginx-certs

create self-signed certificate
openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout nginx-selfsigned.key -out nginx-selfsigned.crt