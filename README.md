sudo apt update     #update system

sudo apt upgrade    #update downloads

sudo apt install ca-certificates curl gnupg lsb-release     #install curl

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg      #download docker

echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null     #set up stable repository

sudo apt update

sudo apt upgrade

sudo apt install docker-ce docker-ce-cli containerd.io     #install docker engine 

sudo usermod -aG docker admin

sudo docker run -d -p 443:443 --name openvas mikesplain/openvas   #run docker
make sure the cpu isn't running at 100%
open firefox and go to https://localhosts/

Set up a target with your ip adress
Go to scans and do a vulnerbility scan


version: '3.3'

services:

openvas:

ports:

- '443:443'
 
 container_name: openvas
 
 image: mikesplain/openvas
