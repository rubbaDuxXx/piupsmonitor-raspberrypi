# piupsmonitor
Programm to monitor the PiUPS+ module for the raspberry pi

This programm is a replacement for the original piupsmon which lacks the
availabity of source code.

**So far the function for shutting down is not tested in reality (as of 2018-11-15). So
use it an your own risk.**

# Reqirements #

## Hardware ##
* Raspberry Pi
* PiUSV+ 

## Software ##

* `libi2c-dev`     \# Bibliothek fuer C


# Install #

### Compile `piusvmonitor.c` ###

    cd src
    gcc -o ../usr/bin/piupsmonitor piupsmonitor.c
    cd ..
    
### Install config file ###

    sudo cp -a etc/piupsmonitor /etc
    
The configuration can be changed in `/etc/piupsmonitor/piupsmonitor.conf`

### Install binary  ###

Copy the binary

    sudo cp -a usr/bin/piupsmonitor

Copy the init-file if you want to start `piupsmonitor` during boot

    sudo cp -a etc/init.d/piupsmonitor /etc/init.d
    
    
    
