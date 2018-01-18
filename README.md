# vagrant-lan
How to make Vagrant box available on LAN

This is just a quick note about how to make Vagrant Box available on the LAN. Also it is important to note that this solution will only work with editing host files on your local machine (it will not work with mobiles etc.)

Inside network section lines below need to be added:

public_network: 192.168.XXX.XXX
type: host-only

They will usually be inserted just below 'private_network:', there might be already 'type' specified but needs to be changed to 'host-only' in order for it to work.
Public network is the IP address that will be available to others on LAN. It needs to match the IP address structure currently used on LAN i.e. 192.168.0.100. However it needs to be IP address that is not already allocated.

Hope this helps.
