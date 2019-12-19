# splunk-siem-usbrun
Splunk SIEM to detect when a drive/disk/device is connected and a script is run

#Logs Capstone project
Use case: a device (optical disc/ drive/ USB/ HID) is plugged in an a malicious script is run



Created a CentOS VM. Installed docker-ce docker-ce-cli and container.io --nobest as latest version of container.io was consistantly skipped which produced errors for docker installs.

docker pull splunk/splunk:latest / docker pull splunk/universalforwarder:latest / docker pull portainer/portainer:latest

installed splunk on 8000 / forwarder on 9997 / portainer on 9000

set -v flag for /var/log:/var/log/CentOS

in splunk, added data - messages (search).
Need to configure access for audit.log (alert)- changed permissions +r - enabled viewing of folder not audit.log
tried ln -s; adding splunk to group; 
