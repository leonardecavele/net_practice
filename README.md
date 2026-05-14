# NetPractice

*This project has been created as part of the 42 curriculum by ldecavel*.

## Description

NetPractice is an introduction to computer networking.

The goal of this project is to understand how machines communicate through a network by configuring IP addresses, subnet masks, routes, and gateways.

The project is made of 10 levels. Each level contains a broken network configuration that must be fixed so that all hosts can communicate correctly.

## Instructions

To start the training interface, run:

```sh
./net_practice/run.sh
```

For each level:

- Configure the IP addresses, subnet masks, routes, and gateways.
- Click `Check again` to verify the configuration.
- Click `Get my config`, to export the configuration file once its valid.

## Submission Details

You can find the 10 exported configuration files at the root of this repository:

```txt
.
├── level10.json
├── level1.json
├── level2.json
├── level3.json
├── level4.json
├── level5.json
├── level6.json
├── level7.json
├── level8.json
├── level9.json
└── ...
```

## Concepts And Resources

AI was used to provide additional explanations and to get a clearer first overview of the project.
[CHATGPT](https://www.chatgpt.com)

### TCP/IP Addressing

TCP/IP is the set of protocols used by machines to communicate on a network.
IP is used to identify machines with IP addresses and to route packets from one network to another.
TCP is used to create reliable communication between programs. It checks that data arrives correctly, in the right order, and retransmits missing data when needed.

[IBM](https://www.ibm.com/docs/en/aix/7.2.0?topic=protocol-tcpip-addressing)
[MICROSOFT](https://learn.microsoft.com/en-us/troubleshoot/windows-client/networking/tcpip-addressing-and-subnetting)

### IP Addresses

An IP address identifies a device interface on a network. Two interfaces can
communicate directly only when they are in the same subnet, unless a router is
used between them.

Example: `192.168.1.10`

[FORTINET](https://www.fortinet.com/resources/cyberglossary/what-is-ip-address#:~:text=IP%20Address%20Definition%20And%20Explanation,use%20the%20internet%20to%20communicate.)
[WIKIPEDIA](https://en.wikipedia.org/wiki/IP_address)

### Subnet Masks

A subnet mask defines which part of an IP address represents the network and
which part represents the host. For example, `255.255.255.0` means that the
first three octets identify the network, and the last octet identifies the host.

The same mask can also be written in CIDR notation:

```txt
255.255.255.0 = /24
255.255.0.0   = /16
255.0.0.0     = /8
```

[WIKIPEDIA](https://en.wikipedia.org/wiki/Subnet)
[YOUTUBE](https://www.youtube.com/watch?v=s_Ntt6eTn94)

### Network Addresses

The network address is the first address of a subnet. It identifies the subnet
itself and cannot be assigned to a host.

Example with `192.168.1.10/24`:

```txt
Network address: 192.168.1.0
```

[WIKIPEDIA](https://en.wikipedia.org/wiki/Network_address#:~:text=A%20network%20address%20is%20an,that%20may%20not%20be%20unique.)

### Broadcast Addresses

The broadcast address is the last address of a subnet. It is used to contact all
hosts in that subnet and cannot be assigned to a host.

Example with `192.168.1.10/24`:

```txt
Broadcast address: 192.168.1.255
```

[WIKIPEDIA](https://en.wikipedia.org/wiki/Broadcast_address#:~:text=A%20broadcast%20address%20is%20a,by%20all%20network%2Dattached%20hosts.)
[IONOS](https://www.ionos.com/digitalguide/server/know-how/broadcast-address/)

### Default Gateways

A default gateway is the router used when a host needs to reach an address that
is outside its own subnet. The gateway address must be reachable from the host's
local network.

[WIKIPEDIA](https://en.wikipedia.org/wiki/Gateway)

### Routing Tables

A routing table tells a machine where to send packets. Each route usually has a
destination network, a subnet mask, and a next hop. If no specific route matches,
the default route is used.

[WIKIPEDIA](https://en.wikipedia.org/wiki/Routing_table)
[GEEKSFORGEEKS](https://www.geeksforgeeks.org/computer-networks/routing-tables-in-computer-network/)

### Routers

Routers connect different networks together. Each router interface belongs to a
specific subnet, and the router forwards packets between those subnets when its
routes are configured correctly.

[WIKIPEDIA](https://en.wikipedia.org/wiki/Router_(computing))
[CLOUDFARE](https://www.cloudflare.com/learning/network-layer/what-is-a-router/)

### Switches

Switches connect devices inside the same local network. They do not route
between different IP networks; they only allow devices in the same subnet to
exchange frames.

[WIKIPEDIA](https://en.wikipedia.org/wiki/Network_switch)

### Local Networks

A local network is a group of devices that can reach each other directly without
going through a router. In practice, this means their IP addresses and masks must
place them in the same subnet.

[WIKIPEDIA](https://en.wikipedia.org/wiki/Local_area_network)

### Internet Routing

Internet routing is the process of forwarding packets across multiple networks
until they reach their destination.

[WIKIPEDIA](https://en.wikipedia.org/wiki/IP_routing)
[SUPERUSER](https://superuser.com/questions/1781245/how-routing-works-on-internet)
[MEDIUM](https://medium.com/@hnasr/network-routing-a-deep-dive-1ecd4757223d)

### OSI Layers

The OSI model is a conceptual model that divides network communication into 7 layers.

```txt
7. Application
6. Presentation
5. Session
4. Transport
3. Network
2. Data Link
1. Physical
```

[CLOUDFARE](https://www.cloudflare.com/learning/ddos/glossary/open-systems-interconnection-model-osi/)
[WIKIPEDIA](https://en.wikipedia.org/wiki/OSI_model)
[GEEKSFORGEEKS](https://www.geeksforgeeks.org/computer-networks/open-systems-interconnection-model-osi/)
