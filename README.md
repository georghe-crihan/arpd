# arpd patch

This patch is to allow for advertising of gateway IPs when its interfaces have
arp disabled (ifconfig -arp) as part of the security measure to bind client
MACs to IPs. This probably would make the network crazy if MAC cloning is used,
but allows for DHCP on the client side, while letting only registered IPs use
the network (provided the firewall and the interfaces on the gateway are configured accordingly).

Meant to be run on FreeBSD 4.11, with ports around July 2005.

The most interesting part to see is in files/patch-arpd.c.self.
