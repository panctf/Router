# Router
## Netgear AC1000 Analysis
### Basic Access
The usual interaction with the router is done through the web portal at www.routerlogin.com

By going to the url www.routerlogin.com/setup.cgi?todo=debug it will open a telnet service on port 23 to connect to. Logging in with the same login as the routerlogin gives shell access to the router.

Some vulnerable processes running on the router but nothing super special.

UPnPd is probably still vulnerable to CVE-2017-1000494 but I don't feel like trying to get the file off the router in order to analyze it. Especially considering it's compiled in MIPS.

Dnrd is running on the box but only listening to the private network. The version they have loaded (2.19) is theoretically vulnerable to CVE-2005-2315 but since it's only listening on the private network it's not really a concern.
