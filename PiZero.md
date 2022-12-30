#  Pi Zero W
IP: <Pi's IP>
U: <Pi's username for ssh>
P: <Pi's password for ssh>
sudo raspi-config

# Pi-Hole
curl -sSl https://install.pi-hole.net | bash

pi-hole site
url:http://pi.hole/admin / <Pi's IP>/admin
pw: <Pi Hole Admin password>

# MQTT Broker
U: <MQTT username>
Pw: <MQTT password>
port: <MQTT Port>


# Node Red
<Node Red IP with Port>