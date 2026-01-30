#!/bin/bash

sudo mv clone-init.sh /usr/local/bin/clone-init.sh
sudo chmod +x /usr/local/bin/clone-init.sh
sudo mv clone-init.service /etc/systemd/system//clone-init.service
sudo systemctl enable clone-init.service
sudo rm -f /etc/sh/ssh_host_*
sudo truncate -s 0 /etc/machine-id
history -c && history -w
sudo shutdown -h now
