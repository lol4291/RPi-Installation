# rpi-installation

Steps for installing docker and setting up drives

# PART A: Installing OS

# PART B: Installing Docker and Docker-Compose
1. Install Docker
> curl -sSL https://get.docker.com | sh
2. Add permission to user
> sudo usermod -aG docker pi
3. Install dependencies [do one by one]
- > sudo apt-get install -y libffi-dev libssl-dev
- >sudo apt-get install -y python3 python3-pip
- >sudo apt-get remove python-configparser
4. Install Docker-compose
> sudo pip3 -v install docker-compose

# PART C: Creating location for drives to mount
1. Create a mount point anywhere. For example in /media as shown.
2. Create a folder as mountpoint. For example WDRED.
3. Take note of the path. For example, if created folder WDRED in /media, then the path is
> /media/WDRED

# PART D: Adding Drives to automount
This enables external harddisk to be read as soon as system starts.
1. Check connected harddisk and names [should look like in picture]
> sudo lsblk
2. Check the id of the harddisk [take  note of UUID]
> sudo blkid
3. Open FSTAB to add the harddrive UUID to autostart [should look like picture once you run]
> sudo nano etc/fstab
4. Add harddisk using the following command [change your UUID and /yourpathhere]
> UUID="your UUID here" /yourpathhere auto defaults,nofail 0 0
5. Final result should look like this.
6. Press Ctrl+X, followed by Y and then press Enter.
