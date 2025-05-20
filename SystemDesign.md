# System Design

## General Steps

- Ask clarifying questions
- Use case diagram
- Public endpoints & Internal endpoints with parameters to be passed
- Bring things like scalability, maintainability into picture (2-3 lines):
  - Do you really need to think about millions of objects in real time?
  - If yes, suggest optimizations & trade-offs
- Class diagrams
- Move towards Database schema:
  - Talk about choice of DBMS: RDBMS or NoSQL
  - Justify your choice
- Coding

---

## **Common Tradeoffs**

- Scalability vs. Performance  
- Vertical vs. Horizontal Scaling  
- Latency vs. Throughput  
- SQL vs NoSQL Databases  
- CAP  
- Read-Through vs Write-Through Cache  
- Batch vs Stream Processing  
- Synchronous vs. Asynchronous Processing  
- Stateful vs Stateless Architecture  
- Normalization vs. Denormalization  
- Monolithic vs. Microservices Architecture  

---

## **Architectures**

- **Peer-to-Peer architecture**
- **Client-server**
- **Serverless Architecture**  
  - Doesn't mean servers are gone; cloud provider manages resource allocation  
  - Developers deploy functions/services  
  - Event-driven model

- **Event Driven Architecture**

---

## **Design Patterns**

- Singleton  
- Factory  
- Observer  
- Strategy  
- Separation of Concerns  

---

## **Common Points to Discuss**

- E/R diagrams  
- Microservices - Connected to Datastores  
- Separate read & write servers  
- Read lock DB replicas  
- Route requests to regional replicas (for latency & performance)  
- Replication to avoid SPOF (Single Point of Failure)  
- Gateways → Load Balancers → Microservices  
- Load balancing can be multi-level: Zone-level → Instance-level  
- Auto Scaling  
- Multi-region deployment  
- Pull vs. Push architectures  
- Asynchronous communication:  
  - Deferring long-running tasks to background queues/message brokers  
- Authentication via session services  
- Caching:  
  - For static content → Read-through cache  
  - For writes → Write-through caches  
- Sharding  
- Feed generation optimization:  
  - Precompute feed on post  
  - Update for LRU users  
  - Skip inactive users to save compute

---

## **Chat Systems**

- Use **XMPP** over **HTTP** for messaging  
- Use **WebSockets** over HTTP Polling  

---

## **Media Handling**

- **BLOBs** for image storage  
- **Transcoding**: Convert input to required formats (e.g., Netflix resolutions)  
- **Adaptive Bitrate Streaming**: Serve lower quality for weak networks  

---

## **Reliability & Fault Tolerance**

- Hystrix for managing microservice endpoints (prevent cascading failures)  
- **To improve Availability**:
  - Redundancy (Replication)
  - Load Balancing
  - Failover mechanisms
  - Disaster recovery plans
  - Monitoring
  - Use Multiple Availability Zones (different data centers)

---

## **CAP Theorem**

- **Consistency**, **Availability**, **Partition Tolerance**  
- **P** = Partition Tolerance → Keep system working despite communication failures  
- In partitioned state → Choose between **C** & **A**

---

## **ACID Transactions**

- **Atomicity**:
  - All-or-nothing
  - Write Ahead Logging (WAL)
- **Consistency**:
  - Primary/foreign/check constraints
- **Isolation**:
  - Transaction independence
  - Isolation Levels: Read Uncommitted, Read Committed, Repeatable Read, Serializable
  - Enforced via Locks, MVCC, Snapshot Isolation
- **Durability**:
  - Data persists after commit despite crashes
  - WAL, Replication, Backups

---

## **Other Concepts**

- **Consistent Hashing**
- **Fault Tolerance**: via Replication
- **Message Queues**:
  - Point-to-Point
  - Publisher/Subscriber
  - Priority Queues

---

## **Why ReactJS is Preferred by Most Companies**

- Startup speed  
- Runtime performance  
- Modularity  

---

## **Useful System Design Videos & Blogs**

- [Parking Lot System Design (YouTube)](https://www.youtube.com/watch?v=NtMvNh0WFVM)  
- [Google Docs Design (YouTube)](https://www.youtube.com/watch?v=2auwirNBvGg)  
- [WhatsApp Design Blog](https://blog.algomaster.io/p/design-a-chat-application-like-whatsapp)  
- [Instagram System Design (YouTube)](https://www.youtube.com/watch?v=VJpfO6KdyWE)  
- [Another Design Resource (YouTube)](https://www.youtube.com/watch?v=psQzyFfsUGU)  
- [Slack Architecture](https://systemdesign.one/slack-architecture/)  
- [YouTube - System Design 1](https://www.youtube.com/watch?v=U0xTu6E2CT8)  
- [YouTube - System Design 2](https://www.youtube.com/watch?v=iRhSAR3ldTw)  
- [YouTube - System Design 3](https://www.youtube.com/watch?v=G32ThJakeHk)

## **Extra**
- [System Design repo](https://github.com/ashishps1/awesome-system-design-resources)
