# Config OpenVPN Server

## prepare server
    apt-get update
    apt-get install openvpn easy-rsa
    gunzip -c /usr/share/doc/openvpn/examples/sample-config-files/server.conf.gz > /etc/openvpn/server.conf

## edit openvpn config
    nano /etc/openvpn/server.conf
Double RSA-Key length (can also be left at "1024"):

    dh2048.pem
VPN Server passes on clients' web traffic to its destination:

uncomment:

    push "redirect-gateway def1 bypass-dhcp"
no more root for OpenVPN:

uncomment:

    user nobody 
    group nobody
