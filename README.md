# routingPPT
Introduction &amp; presentation for routing

# Routers
Routers are the devices on the paths between source hosts and destination hosts. Datagrams are delivered through these paths. A router stores multiple network interfaces connected to difference networks. The routers only check the location of the source host, and implement the corresponding network interface to forward the datagram.

# The routing table
The routing table is a table of connections between the target machine address and the node according to which the router must deliver the message. In reality it is enough that the message is delivered to the network that contains the machine, it is therefore not necessary to store the complete IP address of the machine: only the network identifier of the IP address 
(i.e. the network ID) needs to be stored. 

# Routing protocols
The internet is a collection of connected networks. As a result, all routers do not work in the same way, this depends on the type of network upon which they are found. 

# The RIP protocol
The Routing Information Protocol (RIP) is a vector-distance type protocol which evaluates the shortest network path based on the number of the subnets traversed on the path. When a router receives and forwards a message to the next subnet, the cost of delivering the message increments by 1. After the message is delivered, the router stores the address of the adjacent router into the routing table. The next message can be forwarded directly to a subnet in which the destination host is located, and the path for delivering that message is optimal. RIP evaluates the optimal path based on the number of the subnets between the source and destination, regardless of the connection state of the links.

# The OSPF protocol
OSPF (Open Shortest Path First) is more effective than RIP and is therefore beginning to gradually replace it. It is a protocol route-link type protocol; this means that contrary to RIP, this protocol does not send the number of hops which separates them to the adjacent routers, but the state of the connection which separates them. In this way, each router is capable of sending a card of the state of the network and can as a result choose the most appropriate route for a given message at any time. 
