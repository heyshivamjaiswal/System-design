# System Design

> Learning system design from first principles — both Low Level Design (LLD) and High Level Design (HLD).
* (Still in progress....)

[![MIT License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
![Last Updated](https://img.shields.io/badge/last%20updated-March%202026-blue)

---

## What is this?

This repository is my personal learning journal for system design, built from first principles. It covers both the **structural side** (how classes and components are designed — LLD) and the **architectural side** (how large-scale distributed systems are designed — HLD).

Each topic is written in simple English with diagrams, code examples, comparison tables, and real-world use cases. The goal is that after going through any topic here, you should not need another resource for that concept.

---



### Key concepts covered in LLD

- **OOD** — Modelling real-world problems with classes and objects
- **NVT** — Noun → Class, Verb → Method (technique to extract design from requirements)
- **UML Class Diagram** — Anatomy, access modifiers (`+`, `-`, `#`), stereotypes
- **UML Sequence Diagram** — Lifelines, activation boxes, sync vs async messages
- **Associations** — Inheritance (IS-A), Simple Association (USES), Aggregation and Composition (HAS-A)
- **SOLID** — Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, Dependency Inversion

---


### Key concepts covered in HLD

**Distributed Systems Fundamentals**
- Consistent Hashing — hash ring, virtual nodes, minimal key remapping
- Bloom Filters — probabilistic membership, false positives, real-world use
- Gossip Protocol — peer-to-peer state sync, O(log N) convergence

**Event-Driven Architecture**
- Event Log / Append-Only Log — immutable history, state reconstruction
- Hydration — rebuilding state by replaying events
- Kafka — topics, partitions, consumer groups, offsets, retention

**CQRS (Command Query Responsibility Segregation)**
- Command side vs Query side — separate services, models, databases
- Eventual consistency — the window of inconsistency and when it's acceptable
- AWS context — SQS, SNS, Lambda, DynamoDB mapping

**Back-of-Envelope Estimation**
- Essential conversions (KB, MB, GB, TB, PB)
- Latency numbers every engineer must know
- QPS estimation and storage estimation patterns

**System Design Interview**
- Requirements clarification framework (Users, Scale, Performance, Cost)
- API design from first principles (verbs → generalise → add parameters)
- Non-functional requirements and CAP theorem decision
- Processing Service internals — Aggregator, Checkpointing, Partitioning
- Data ingestion path — API Gateway → Load Balancer → Kafka → Processing → DB

---

## Learning Path

If you are starting from scratch, follow this order:

```
1. LLD — OOD Basics        → understand how to model problems as classes
2. LLD — UML Diagrams      → learn the visual language for design
3. LLD — SOLID Principles  → learn how to write maintainable code design
      ↓
4. HLD — System Design Basics     → DNS, CDN, Load Balancer, Caching
5. HLD — Distributed Systems      → Hashing, Bloom Filters, Gossip
6. HLD — EDA & CQRS               → Event-Driven patterns
7. HLD — Back-of-Envelope         → Estimation skills
8. HLD — Interview Blueprint      → Put everything together
```

---

## External Resources

Resources that influenced or complemented this study:

| Resource | Type | Topic |
|----------|------|-------|
| [System Design Interview – Alex Xu](https://www.amazon.com/dp/B08CMF2CQF) | Book | HLD interview prep |
| [Designing Data-Intensive Applications – Kleppmann](https://dataintensive.net/) | Book | Deep distributed systems |
| [System Design Interview Course – Educative](https://www.educative.io/courses/grokking-the-system-design-interview) | Course | HLD patterns |
| [ByteByteGo](https://bytebytego.com/) | Newsletter / Videos | Visual HLD explanations |
| [refactoring.guru](https://refactoring.guru/) | Website | Design patterns and SOLID |

---

## Contributing

Found a mistake, have a better example, or want to add a new topic? Pull requests are welcome.

1. Fork the repository
2. Create your branch (`git checkout -b topic/add-new-concept`)
3. Commit your changes (`git commit -m 'Add: explanation for X'`)
4. Push to the branch (`git push origin topic/add-new-concept`)
5. Open a Pull Request

---

## License

MIT — free to use, share, and build on.

---

<p align="center">
  Built while learning. Mistakes are part of the process.
</p>
