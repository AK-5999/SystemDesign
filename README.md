# SystemDesign
# System Design Summary

This document provides a quick reference for key concepts and components in system design.

<img width="849" height="1078" alt="Screenshot 2025-10-07 235439" src="https://github.com/user-attachments/assets/cc472ba1-097e-46ed-9ee3-d4914635bba4" />


---

## 1. **Single Server System**
- **Definition**: A basic system setup using one server for all operations.
- **Use**: Small-scale systems, testing, and development.
- **Limitations**: Scalability, performance, and reliability issues.
- **Solutions**: Load balancing, horizontal scaling, database sharding.

---

## 2. **Database Types**
- **SQL Databases**: Relational databases using structured query language (e.g., MySQL, PostgreSQL).
- **NoSQL Databases**: Non-relational, often used for large-scale, unstructured data (e.g., MongoDB, Cassandra).
- **Graph Databases**: Used for relationships between entities (e.g., Neo4j).
- **Key-Value Stores**: Stores data as key-value pairs (e.g., Redis, DynamoDB).
- **Column-Oriented Databases**: Used for storing large datasets in columns (e.g., HBase).

---

## 3. **Monolithic Architecture**
- **Definition**: A single, unified codebase where all components of the system are tightly integrated.
- **Pros**: Simplicity, easier to deploy.
- **Cons**: Difficult to scale, maintain, and test as the system grows.

---

## 4. **Microservices Architecture**
- **Definition**: A decentralized approach with each service running independently and communicating over a network.
- **Pros**: Scalability, flexibility, independent development.
- **Cons**: Complexity, inter-service communication overhead.

---

## 5. **Vertical Scaling**
- **Definition**: Increasing the resources (CPU, RAM) of a single server.
- **Pros**: Simplicity.
- **Cons**: Limits to scalability, single point of failure.

---

## 6. **Horizontal Scaling**
- **Definition**: Adding more servers or instances to distribute load.
- **Pros**: Scalable, fault-tolerant.
- **Cons**: Complexity in distribution, data synchronization.

---

## 7. **Load Balancer**
- **Definition**: A device or service that distributes incoming network traffic across multiple servers.
- **Types**:
  - **Round Robin**: Distributes traffic evenly.
  - **Least Connections**: Sends traffic to the server with the least active connections.
  - **IP Hashing**: Routes requests based on IP address.
  - **Weighted Round Robin**: Distributes traffic based on server capacity.

---

## 8. **Database Replication**
- **Definition**: The process of copying data from one database server to another to ensure data availability.
- **Types**:
  - **Master-Slave Replication**: One primary server (master) with one or more secondary servers (slaves).
  - **Master-Master Replication**: Both servers are capable of writing data.
  - **Multi-Master Replication**: Multiple servers handling reads and writes.

---

## 9. **Caching**
- **Definition**: Temporarily storing frequently accessed data to reduce database load and increase performance.
- **Types**:
  - **Memory Caching**: Uses RAM for storing cached data (e.g., Redis).
  - **Distributed Caching**: Caching across multiple systems (e.g., Memcached).
  - **Content Delivery Network (CDN)**: Caching static content closer to end users (e.g., Cloudflare).

---

## 10. **Content Delivery Network (CDN)**
- **Definition**: A network of geographically distributed servers that cache and serve content to users based on their location.
- **Use**: Accelerates content delivery by reducing latency and offloading server load.

---

## 11. **Stateful vs Stateless Architecture**
- **Stateful**: The system remembers the state of user sessions or data (e.g., databases, session cookies).
- **Stateless**: Each request is independent and does not retain previous session information (e.g., RESTful APIs).

---

## 12. **Data Centers & GeoDNS**
- **Data Centers**: Physical or virtualized facilities for hosting servers and infrastructure.
- **GeoDNS**: DNS system that routes traffic to the nearest or most appropriate data center based on geographic location.

---

## 13. **Message Queue**
- **Definition**: A system that enables asynchronous communication by temporarily storing messages between producers and consumers.
- **Types**:
  - **Queue**: One-to-one communication between producer and consumer.
  - **Publish-Subscribe**: One-to-many communication.
  - **Work Queue**: Distributes tasks to workers.
- **Examples**: RabbitMQ, Kafka, Amazon SQS.

---

## 14. **Metrics**
- **Definition**: Quantitative measures used to track performance and system health.
- **Types**:
  - **CPU Usage**
  - **Memory Usage**
  - **Disk I/O**
  - **Request Rate**
  - **Error Rate**
  - **Availability/Uptime**

---

## 15. **Monitoring**
- **Definition**: Continuous observation of a system to detect issues and ensure proper functioning.
- **Types**:
  - **Infrastructure Monitoring**
  - **Application Performance Monitoring (APM)**
  - **Log Monitoring**
  - **Real-Time Monitoring**

---

## 16. **Logging**
- **Definition**: Recording system events, errors, and status for troubleshooting and audit purposes.
- **Types**:
  - **Application Logs**
  - **System Logs**
  - **Access Logs**
  - **Event Logs**
- **Tools**: ELK Stack, Splunk, Graylog.

---

## 17. **Automation**
- **Definition**: Automating repetitive tasks to improve efficiency and consistency in system management.
- **Types**:
  - **Infrastructure Automation** (e.g., Terraform, Ansible)
  - **Deployment Automation** (e.g., Jenkins, GitLab CI)
  - **Scaling Automation** (e.g., Kubernetes HPA)
  - **Incident Remediation** (e.g., PagerDuty)
  - **Log-Based Automation** (e.g., Fluentd)

---

## 18. **Key System Design Principles**
- **Scalability**: System’s ability to handle growth (traffic, users, data).
- **Reliability**: Ensuring the system can handle failure and continue functioning.
- **Availability**: The proportion of time the system is operational and accessible.
- **Performance**: How quickly and efficiently the system processes requests.
- **Maintainability**: How easy it is to maintain and update the system.
- **Decoupling**: Designing systems where components are independent, reducing dependencies.

---

## 19. **Best Practices**
- **Failover**: Ensure the system has backup mechanisms in place for redundancy.
- **Distributed Systems**: Leverage microservices, database sharding, and replication for fault tolerance.
- **Caching**: Use caching to improve performance by reducing database load.
- **Health Checks**: Implement health checks for systems and services.
- **Alerting & Monitoring**: Set up thresholds for metrics and enable real-time monitoring and alerts.
- **Automation**: Automate routine tasks like deployment, scaling, and incident remediation.

---
