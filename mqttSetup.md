# Broker Setup
1. Install Mosquitto 
    - `sudo apt-get install mosquitto -y`
    - `sudo apt-get install mosquitto-clients`
2. Configure Mosquitto
    - `sudo nano /etc/mosquitto/mosquitto.conf`

    - pid_file /var/run/mosquitto.pid
    - persistence true
    - persistence_location /var/lib/mosquitto/

    - log_dest file /var/log/mosquitto/mosquitto.log

    - allow_anonymous false
    - password_file /etc/mosquitto/pwfile
    - listener <MQTT Port> (1833)
3. Setup Mosquitto credentials
    - `sudo mosquitto_passwd -c /etc/mosquitto/pwfile <USERNAME_HERE>`
4. If `unable to write pid file` then give priveleges to mosquitto user
    - Following these instructions you would use this in console: `sudo chown mosquitto /var/run`

# paho-mqtt client test setup
- `sudo pip3 install paho-mqtt`
- Create Connection_Test python file as seen in Desktop/PythonCode/MQTT 


# useful commands
- `sudo netstat -pant | grep <port number or ip here>`
    - Used this to find what was using port 1883 (or whatever you MQTT Port is)


# database stuffs
1. https://pimylifeup.com/raspberry-pi-mysql/
2. https://www.2daygeek.com/check-mysql-mariadb-database-table-size-in-linux/
3. https://dev.mysql.com/doc/connector-python/en/connector-python-example-cursor-transaction.html
4. https://mariadb.com/kb/en/date-time-functions/
5. https://realpython.com/python-string-formatting/
6. https://overiq.com/mysql-connector-python-101/inserting-data-using-connector-python/