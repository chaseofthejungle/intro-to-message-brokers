# Intro to Message Brokers
When choosing a message brokering technology, organizational use case can simplify the decision-making process greatly--or even lead to a quick answer. However, other factors are relevant and should, if not must, be considered: scalability needs, throughput and latency performance requirements, potential compatibility and integrations with the organization's protocol stack, willingness to take on a medium-to-high learning curve technology, and long-term data storage and logging needs.
  
More details on five prominent brokering protocols are summarized below:
  
| Characteristic | Kafka | RabbitMQ | Pulsar | ActiveMQ | NATS |
| ---- | ---- | ---- | ---- | ---- | ---- |
| Intended Use | Large data pipelines, streaming in real-time with high analytics and extensive event-related requirements. | Light message queueing and task scheduling, advanced routing. | Enterprise systems, multi-tenant operations, georeplication. | Messaging for enterprise-level, Java-based organizations. | Microservices and IoT integrations that must communicate seamlessly. |
| System Architecture | Broker, partition, and replica based distribution. | Push-based messaging via a centralized broker. | Distributed, with tiered storage and native replication ability. | Supports many protocols with its centralized broker. | P2P connections. Broker not required. |
| Scalability | Horizontally partitioned for high scalability. | Limited by design. | Horizontal scalability. | Somewhat scalable. | High scalability (for lightweight environments). |
| Protocol(s) | Custom. | AMQP, MQTT, STOMP. | Kafka APIs, with some additional native features. | AMQP, JMS, MQTT, STOMP. Can use legacy protocols. | Native NATS protocol. | 
| Performance | Large throughputs. | Medium throughputs. | Low latency, but high throughputs. | Medium throughputs. | Very low latency, but for smaller messages. |
| Message Retention | Customizable log retention. | Message acknowledgment and permanent storage. | Tiered storage (by cost). | Permanent storage (caching optional). | Permanent storage is optional. |
| Ordering | Partition-based maintenance. | Configuration required. | Partition-based maintenance. | Minimal, but customizable. | Not a native feature. |
| Learning Curve | High. | Low (and widely supported). | Medium, dependent on configurations. | Low. | Very Low. |
