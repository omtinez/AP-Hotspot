AP-Hotspot
==========

Automatically creates an infrastructure (Access Point mode) wireless hotspot in Ubuntu that should work with Android and Windows Phone devices

Usage
----
    ap-hotspot [argument]

        start          start wireless hotspot
        stop           stop wireless hotspot
        restart        restart wireless hotspot
        enable         enable wireless hotspot service
        disable        disable wireless hotspot service
        configure      configure hotspot
        debug          start with detailed messages



Install
-------
On **Debian and Ubuntu** run

    sudo apt-get update
    sudo apt-get install libnotify-bin iw dnsmasq
    sudo make install
    
You can use the PREFIX make parameter to change the install directory

    sudo make install PREFIX=/usr/sbin
    
If you want to start AP-Hotspot at boot and you are using **Debian Wheezy** you may need to install a recent systemd version from the backports

    sudo sh -c \
    "echo 'deb http://ftp.us.debian.org/debian wheezy-backports main' > \
     /etc/apt/sources.list.d/wheezy-backports.list"
    sudo apt-get update
    sudo apt-get install -t wheezy-backports systemd
    
