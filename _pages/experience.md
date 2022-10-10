---
layout: archive
title: "Experience"
permalink: /experience/
author_profile: true
---

{% include base_path %}

* **Bharat Tech Labs, India**
  * Position: Full Stack Engineer
  * Duration: September 2021 - July 2022
  * Work Description:
     * Project Lead for [Monitor](https://monitor.keytoz.com)
        * A monitoring tool for HTTPS endpoints along with SIP(VoIP) registrations.
            
          * Initial responsibilties included extensive market research, scalable and performant backend architecture, user-friendly front-end design decisions. 
            
          * Inspired by the flexibility and potential of event-driven architectures, Monitor's loosely coupled backend consisted of a myriad of BullMQ-worker pairs each handling a single responsibility i.e Target Distribution, Axios calls, Incident Creation, Escalation Alerts and finally to Email workers. All of these could not have been possible without an efficient DB design which would also be helpful for system restoration in failure scenerios.

          * With the number of workers growing rapidly, I was also responsible for developing Github WorkFlows for these containerized workers which would allow automated build and deployment. Additionally, to adhere to best software design practices, docker image tags followed semantic versioning.

          * Removed redundant code from all workers by building a base package. This package follows the [Factory Pattern](https://en.wikipedia.org/wiki/Factory_method_pattern) for its advantages of extensibility. 

          * Deployed Cassandra Multi-region cluster for high frequency of write requests which Postgres could not handle during a request spike. Additionally helped with setting up Stargate, a GraphQL API gateway for CassandraDB.
      
      * Successfuly upgraded a production Kubernetes cluster of [Dolphin](https://dolphin.evs7.com/) with minimal downtime. 

           * Created ClusterConfigs for eksctl, cluster roles for AWS-Lambda and cluster-admin.
           * Wrote Dolphin deployment YML, set-up of HPA(Pod Scaling, Same Node) and Cluster Autoscaler(Pod Scaling across Nodes). 
           * Created Network Load Balancer(NLB), managed Node Groups and modified CI/CD pipeline for this new setup.
           * Utilized ConfigMaps and Persistent Storage for Prometheus to collect cluster-wide metrics. BlackBox Exporters were used to probe internal API endpoints. Prometheus was configured to automatically discover new pods through its service discovery functionality.

  * Skills acquired: Kubernetes, Message Queues, Redis, Cassandra, VueJS, TypeScript, PostgreSQL and GraphQL.
  * Links: [Website](https://bharattechlabs.com/)
  
* **Omni Automation, India**
  * Position: Research Intern
  * Duration: January 2021 - June 2021
  * Work Description: 
      * Measured electrical parameters of a railway yard in an isolated and a non-contact manner.
      * Transmitted acquired data to a web server that logs and continuously accepts data via MQTT protocol.
      * Built a web application that can display collected data in realtime as well as history(graphical) and exceptions  the same as per requests from the user.
      * Took data from web application and trained a recurrent neural network model to predict various track circuit parameters.
  * Skills acquired: MQTT, RNN, Web Socket and JS.
  * Links: [Website](https://omniautomation.in/)
