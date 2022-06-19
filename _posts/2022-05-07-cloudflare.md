---
title: 'Cloudflare, Cassandra and the ButterFly effect'
date: 2022-05-07
permalink: /posts/2022/05/07/
tags:
  - Computer Networks
  - Distributed storage
  - Chaos theory
---

My weekend exploration

### CloudFlare 

Read a CloudFlare blog about the recent internet outage in Kherson, Ukraine. 
Apparently Russian had replaced the Ukrainian ISP and connected for some time to the Russian internet network thus they were able to monitor it entirely. CloudFlare showed a graph in which they depicted a spike in their Moscow Data Center.

### Cassandra

* Difference between Simple Strategy and Network Topology Strategy is more conspicuous. Simple Strategy will choose the next irrespective of its DC/RACK location, on the other hand NTS will be aware of the Network Topology(through our chosen snitch) and will group based on DC/Rack. Performance is same for SS and NTS in our case.

* NTS power is revealed when we put suffixes(cassandra-rackdc.properties)  to form virtual groups for asymmetrical replication groups i.e some servers could be used for HA data and some other tasks where latency is acceptable we can query it from other nodes.

* Learned about consistency levels and still could not find the reason behind last week’s error.
When hinted handoff is turned on, the coordinator stores data of replica nodes that are not responding for 3hrs after which it flushes it. 

* Cassandra read path is more complex than write path. Anyone can be a coordinator node in a cluster.
More num tokens has an inverse effect on the fault tolerance of the cluster.

### Butterfly Effect

Learned about the science of butterfly effect(Chaos). It all started few years after Principia was released, when someone challenged Newton to find a solution to the three-body problem. Poincare termed it chaos. It was picked up again when a meteorologist whose name I forgot was trying to predict the state of the atmosphere based on some 12 variables(temp, pressure..). When he was redoing his calculations rather than doing it from start he took half observations from last calculation and found the data was completely divergent. This started the chaos theory, small irrelevant change and a huge impact down the lane. Swinging of a double pendulum is chaotic, its phase-angle plot reveals a butterfly like shape hence the name. They are also linked to FRACTALS.
