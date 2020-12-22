# rpi-installation

Steps for installing docker and setting up drives

# PART A: Installing OS

# PART B: Installing Docker and Docker-Compose
1. Install Docker
> curl -sSL https://get.docker.com | sh
2. Add permission to user
> sudo usermod -aG docker pi
3. Install dependencies [do one by one]
-> sudo apt-get install -y libffi-dev libssl-dev
->sudo apt-get install -y python3 python3-pip
->sudo apt-get remove python-configparser
4. Install Docker-compose
> sudo pip3 -v install docker-compose
