# Intro to Message Brokers
When choosing a message brokering technology, organizational use case can simplify the decision-making process greatly--or even lead to a quick answer. However, other factors are relevant and should, if not must, be considered: scalability needs, throughput and latency performance requirements, potential compatibility and integrations with the organization's protocol stack, willingness to take on a medium-to-high learning curve technology, and long-term data storage and logging needs.
  
More details on five prominent brokering protocols are summarized below:
  
| Characteristic | [Kafka](https://kafka.apache.org/) | [RabbitMQ](https://www.rabbitmq.com/) | [Pulsar](https://pulsar.apache.org/) | [ActiveMQ](https://activemq.apache.org/) | [NATS](https://nats.io/) |
| ---- | ---- | ---- | ---- | ---- | ---- |
| `Intended Use` | Large data pipelines, streaming in real-time with high analytics and extensive event-related requirements. | Light message queueing and task scheduling, advanced routing. | Enterprise systems, multi-tenant operations, georeplication. | Messaging for enterprise-level, Java-based organizations. | Microservices and IoT integrations that must communicate seamlessly. |
| `System Architecture` | Broker, partition, and replica based distribution. | Push-based messaging via a centralized broker. | Distributed, with tiered storage and native replication ability. | Supports many protocols with its centralized broker. | P2P connections. Broker not required. |
| `Scalability` | Horizontally partitioned for high scalability. | Limited by design. | Horizontal scalability. | Somewhat scalable. | High scalability (for lightweight environments). |
| `Protocol(s)` | Custom. | AMQP, MQTT, STOMP. | Kafka APIs, with some additional native features. | AMQP, JMS, MQTT, STOMP. Can use legacy protocols. | Native NATS protocol. | 
| `Performance` | Large throughputs. | Medium throughputs. | Low latency, but high throughputs. | Medium throughputs. | Very low latency, but for smaller messages. |
| `Message Retention` | Customizable log retention. | Message acknowledgment and permanent storage. | Tiered storage (by cost). | Permanent storage (caching optional). | Permanent storage is optional. |
| `Ordering` | Partition-based maintenance. | Configuration required. | Partition-based maintenance. | Minimal, but customizable. | Not a native feature. |
| `Learning Curve` | High. | Low (and widely supported). | Medium, dependent on configurations. | Low. | Very Low. |

<br />
The Apache message broker 'Kafka' is a common solution, if not the gold standard, for enterprise-level, instantaneous/real-time event streaming (especially in distributed environments with an abundance of data pipelines). Prior to investigating several of its use cases, it is worth considering its inherent advantages over some other event brokering platforms:

* Order guaranteeing provides peace-of-mind and far fewer headaches than many other solutions do for heavily pipelined environments.
* The pairing of fault tolerance mechanisms *with* data replication for high availability assurance.
* The ability to store messages for a long time, if an organization wills it (sets up the appropriate configurations).
* The combination of high-level throughput (such as millions of messages per second), very low latency (less than 10 milliseconds), and assurances of horizontal, partition-based scalability.
* Support for rapidly changing/modified schemas.
<br />
Furthermore, there are at least several factors a team should evaluate before deciding whether Kafka is the right message broker solution for their organization:

* Their system resource requirements and whether Kafka corresponds to them. 
* The role of schemas and schema management in their system and operations. 
* If their team is ready to implement, maintain, and respond to Kafka’s alert and monitoring systems and strategic topic configuration and partition design controls (and utilize them to their potential).
* If Kafka’s ‘consumer group’ (for message processing, based on topic) mechanism matches their system’s needs/operations.
* If Kafka can be integrated into their organizational backup and disaster recovery plans, and if it makes sense to do so.


Finally, several of the popular use cases for Kafka include:

* Message Queueing
  + Message delivery is reliable and long-term data storage can be enabled and configured per organizational need.
  + Message orders can be guaranteed (assured) at the partition-level.
  + A reliable message replay feature can be set up.
  + ‘Consumer’ and ‘producer’ mechanisms are decoupled (promoting autonomous/independent communications among components), for high scalability.
  + More than one consumer group, with various processing speeds, can be enabled.
* Instant/Real-Time Analytics
  + This is a product of consumer/producer decoupling (and the resulting high scalability) and the allowance of various consumer groups.
  + Real-time business metric data can be monitored through dashboards.
  + Topic partitioning processes events quickly.
  + Data can be aggregated and computations windowed instantly/in real-time.
* Processing of Data Streams
  + Topic-based partitions allow for consistently large throughput levels.
  + Instant processing of rapidly, directly streamed data (through the use of Apache's Spark technology) is a Kafka specialization.
  + Social media platform data can be operated upon quickly (even for large web assets such as TikTok and Facebook).
  + Data streams can be used for machine learning models and training.
  + High volume data streaming can be done seamlessly/without interruption.
* System Migrations
  + Cutover can be handled on a configurable pace.
  + Data/systems can be rolled back with ease.
  + Migrations can be accomplished without downtime and data reconciliation for perfect data consistency.
  + Dual-write data patterns are supported.
* Alerting/Monitoring
  + Metrics can be instantly gathered from microservices/web assets and compared against baseline (even when changes are incremental).
  + System health/posture can be monitored in real-time via dashboard tools.
  + Alerts can notify teams as soon as possible when outlier data/events occur.
  + Predictive monitoring and high-level event data stream processing are configurable.
* Log Aggregation
  + Kafka’s Connect tool provides real-time log processing, and allows for aggregated log analysis.
  + More than one downstream consumer can be enabled and logged at once, even in high volume scenarios.
  + Insights are provided by analytics engines, and data can be fed to them in real-time.
  + Logs can be stored in a centralized manner (even from distributed systems/environments) for secure, long-term data persistence.
* Support for Change Data Capture (CDC)
  + Data integrity/consistency supported across systems.
  + Changes to databases are accounted for instantly/in real-time, with incremental changes monitored and recorded.
  + Kafka Connect’s ‘sink connectors’ assist with caching, searching, and replicating. 
* Data Replication
  + Replication across data centers is supported, as well as instantaneous data mirroring (crucial for backups and disaster recovery).
  + Data distribution can be handled via clustering.
  + Data can be synchronized across databases and consistently delivered.
  + Kafka reduces single point of failure occurrences and provides high redundancy (the preceding three points provide examples of how). 

TODO: Add notes on IBM MQ.
