## Route calculation:
- prefix length
- Admin distance
- Metric

## Admin distance
Routing protocol | Cisco Default AD
- | -
Connected | 0
Static | 1
Eigrp summary route | 5
EBGP | 20
EIGRP (internal) | 90
IGRP | 100
OSPF | 110
ISIS | 115
RIP | 120
EIGRP (external) | 170
IBGP | 200

## Static routing type
- Direct ip route x.x.x.x m.m.m.m <int>
- Recursive ip route x.x.x.x m.m.m.m <ip>
- Fully specified ip route x.x.x.x m.m.m.m <int> <ip> 
- Floating static route is configured with an AD value of 1 to 255

```
Configuring a directly attached static route to an interface that uses ARP (that is, Ethernet) causes problems and is not recommended. The router must repeat the ARP process for every destination that matches the static route, which consumes CPU and memory.
```

```
Recursive static routes require the route’s next-hop address to exist in the routing table to install the static route into the RIB. A recursive static route may not resolve the next-hop forwarding address using the default route (0.0.0.0/0) entry. The static route will fail next-hop reachability requirements and will not be inserted into the RIB.
```
