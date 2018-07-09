# routingPPT
Introduction &amp; presentation for routing

# Routers
Routers are devices which make it possible to "choose" the path that datagrams will take to arrive at the destination. 
They are machines with several network interface cards each one of which is linked to a different network. So, in the simplest configuration, the router only has to "look at" what network a computer is located on to send datagrams to it from the originator. 

# The routing table
The routing table is a table of connections between the target machine address and the node according to which the router must deliver the message. In reality it is enough that the message is delivered to the network that contains the machine, it is therefore not necessary to store the complete IP address of the machine: only the network identifier of the IP address 
(i.e. the network ID) needs to be stored. 

# Routing protocols
The internet is a collection of connected networks. As a result, all routers do not work in the same way, this depends on the type of network upon which they are found. 

# The RIP protocol
RIP means Routing Information Protocol. It is a Vector Distance type protocol, i.e. each router communicates to the other routers the distance which separates them (the number of hops which separates them). So, when a router receives one of these messages it increments this distance by 1 and sends the message to directly accessible routers. In this way, the routers can then keep the optimal route of a message by storing the next router address in the routing table in such a way that the number of hops to reach a network is kept to a minimum. However this protocol only takes into account the distance between two machines in terms of hops and does not consider the state of the connection so as to select the best possible bandwidth. 

# The OSPF protocol
OSPF (Open Shortest Path First) is more effective than RIP and is therefore beginning to gradually replace it. It is a protocol route-link type protocol; this means that contrary to RIP, this protocol does not send the number of hops which separates them to the adjacent routers, but the state of the connection which separates them. In this way, each router is capable of sending a card of the state of the network and can as a result choose the most appropriate route for a given message at any time. 
