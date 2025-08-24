# system_design && java_design_patterns

- Nice Youtuber :- Concept && Coding - by Shrayansh (Many things here)

- Extras:- AWS Bucket, Elastic, with Mathematics

#################################################################################################################################

➤ 𝗖𝗹𝗮𝗿𝗶𝗳𝘆 𝘁𝗵𝗲 𝗥𝗲𝗾𝘂𝗶𝗿𝗲𝗺𝗲𝗻𝘁𝘀: 𝗪𝗵𝗮𝘁 𝗔𝗿𝗲 𝗬𝗼𝘂 𝗕𝘂𝗶𝗹𝗱𝗶𝗻𝗴?
- The first step is to understand what’s being asked fully. Don’t rush into designing before you know the scope.
- Who will use the system?
- What will they use it for?
- How many users are expected?
- What will the system do?
- What kind of data will it handle, and how much?
- How many requests per second should it support?

➤ 𝗗𝗲𝘀𝗶𝗴𝗻 𝗛𝗶𝗴𝗵-𝗟𝗲𝘃𝗲𝗹 𝗔𝗿𝗰𝗵𝗶𝘁𝗲𝗰𝘁𝘂𝗿𝗲
- Outline the high-level architecture. (sketching out the key components and how they interact with each other)
- Identify major components: Break down the system into key parts. In a social media app, for example, you’d have user profiles, posts, comments, and notifications.
- Show connections: Explain how these components communicate, whether through APIs, databases, load balancers, or caching layers.
- Justify your choices: Don’t just present a design; explain why.

➤ 𝗙𝗼𝗰𝘂𝘀 𝗼𝗻 𝗞𝗲𝘆 𝗖𝗼𝗺𝗽𝗼𝗻𝗲𝗻𝘁𝘀
- For ex, a URL shortening service:
- How will you generate and store shortened URLs?
- What hashing technique will you use (e.g., MD5, Base62)?
- How will you handle hash collisions?
- What kind of database will you use (SQL or NoSQL)?
- How will you store and retrieve the data efficiently?

➤ 𝗦𝗰𝗮𝗹𝗶𝗻𝗴: 𝗛𝗮𝗻𝗱𝗹𝗲 𝗚𝗿𝗼𝘄𝘁𝗵 𝗮𝗻𝗱 𝗧𝗿𝗮𝗳𝗳𝗶𝗰
- Think about how the system will scale.
- What happens when the user base grows from 1,000 to 1 million?

When discussing scalability, always consider trade-offs. For ex: Caching can improve performance but might introduce complexity in keeping data up-to-date.

Quick Calculations: Make quick estimates for data storage, traffic, and basic numbers like latency and data sizes.

#################################################################################################################################

Edge Servers, DNS, CDN (OpenConnect), API Gateway (Zuul), Circuit Breaker, LB, Aggregation Service, Instrumentation, etc. drawing from my experience at VideoVerse, Velvet, LambdaTest, and Tekion
c. I fumbled a bit choosing between S3 vs EFS for large video storage. Later realized S3 is ideal due to chunking and adaptive stream generation
Takeaway: Should’ve just mentioned S3 for block storage and cost-effectiveness
d. API Contracts and DB Models

######################################################################################

If I were your interviewer in a System Design interview, here’s how I’d evaluate your answers — based on these 40 core fundamentals:

1. Scalability – Vertical vs horizontal; default to stateless horizontal scale
2. Latency & Throughput – Know P50/P95/P99 and tradeoffs
3. Capacity Estimation – Estimate QPS, storage, bandwidth
4. Networking Basics – TCP, HTTP/HTTPS, TLS, UDP, DNS
5. SQL vs NoSQL – Decide by access patterns, joins, consistency
6. Data Modeling – Structure to optimize hot queries
7. Indexing – Right indexes help reads, wrong ones hurt writes
8. Normalization – Normalize for writes, denormalize for reads
9. Caching – App/DB/CDN; write-through/back, TTLs
10. Cache Invalidation – TTLs, versioning, stampede protection
11. Load Balancing – L4/L7, RR, least-connections, hashing
12. CDN & Edge – Serve static content near users
13. Sharding – Hash/range/geo; handle hot keys, rebalancing
14. Replication – Sync/async, leader/follower, read replicas
15. Consistency Models – Strong, eventual, causal
16. CAP Theorem – In partition, pick A or C
17. Concurrency – Locks, MVCC, retries
18. Multithreading – Pools, contention, switching
19. Idempotency – Same request, same effect
20. Rate Limiting – Fairness and protection
21. Queues & Streams – Kafka, RabbitMQ; smooth spikes
22. Backpressure – Manage slow consumers/load shedding
23. Delivery Semantics – At-most/least/exactly-once
24. API Design – REST vs gRPC; human vs machine optimized
25. API Versioning – Additive only; never break clients
26. AuthN & AuthZ – OAuth2, JWT, RBAC/ABAC
27. Resilience – Circuit breakers, timeouts, retries
28. Observability – Logs, metrics, traces, SLI/SLO
29. Health Checks – Detect failures, auto-replace
30. Redundancy – Avoid SPOFs; use multi-AZ/region
31. Service Discovery – Dynamic endpoints, central config
32. Deployment – Canary, blue/green, rollbacks
33. Monolith vs Microservices – Split only if ops cost justified
34. Distributed Transactions – Use sagas, avoid 2PC
35. Event Sourcing/CQRS – Append-only logs, split models
36. Consensus – Raft, Paxos, quorum reads/writes
37. Data Privacy – Encryption, GDPR/CCPA
38. Disaster Recovery – Backups, RPO/RTO, test it
39. Serialization – JSON, Avro, Proto
40. Real-Time Delivery – Polling, SSE, WebSockets

######################################################################################

Machine Learning:-
1. Build a youtube video summarizer with LLMs - https://lnkd.in/gyxcvKQN
2. Build a House Prediction App End to End deployed project - https://lnkd.in/gbUxPRJq
3. Build an Image Captioning Model using CNN + LSTM - https://lnkd.in/gFKuDr3W
4. Build your own chatbot using ML - https://lnkd.in/gWr6wWah
5. Implement regression from scratch - https://lnkd.in/gtj7GhbE
6. Finetuning project on llama model - https://lnkd.in/gDRYgyGS
7. Finetuning project on personal dataset on llama model - https://lnkd.in/gPuqrqJ8
8. MCP Project End to End + Explanation of MCP in great detail (MCP = Model Context Protocol) (Newest addition) https://lnkd.in/gBxpHbjS
9. RAG Project End to End + Explanation of RAG in great detail (RAG = Retrieval Augmented Generation) (Newest addition) https://lnkd.in/gBHyMhtf

#######################################################################################

Terms:-
- Latency

#############################

Dear software engineers, you'll definitely thank yourself later if you spend time learning this today:

⥽ Redis
> Your AI tools can help you write code, but when it comes to fast data access and handling spikes, Redis knowledge will save you in prod.

⥽ Docker & Kubernetes
> Knowing how to build, ship, and scale with Docker and K8s will make you valuable even if you’re using Copilot for code.

⥽ Message Queues (Kafka, RabbitMQ, SQS, etc.)
> When you need to decouple services or handle unpredictable spikes, nothing beats message queues. AI will not explain why your system dropped messages at 3AM, but you’ll know if you actually practiced queues.

⥽ ElasticSearch
> Search is not just about matching keywords. If you ever need to build search, logs, or analytics at scale, Elastic will come up.

⥽ WebSockets
> For anything real-time, chat, games, live dashboards, WebSockets are key. Your AI tools won’t design a fault-tolerant, low-latency messaging layer for you. Only learning, building, and breaking things will.

⥽ Distributed Tracing
> In a microservices jungle, tracing lets you see exactly where requests slow down or fail. AI will tell you “add tracing,” but you have to know where and how to trace.

⥽ Logging & Monitoring
> Nobody wants to get a “site down” call at midnight with zero logs. Learn what, when, and how to log. Monitoring will help you detect issues before users even see them.

⥽ Concurrency & Race Conditions
> Even the best AI misses subtle concurrency bugs. Learn how to write and review multithreaded or async code. You’ll save days in debugging.

⥽ Load Balancers & Circuit Breakers
> When your backend goes down or traffic spikes, these patterns keep your service up. Theory is easy, handling real-world outages is something you have to experience.

⥽ API Gateways & Rate Limiting
> If you ever ship a public API, you’ll thank yourself for knowing this. Otherwise, get ready for abuse, cost overruns, or worse.

⥽ SQL vs NoSQL
> Not every problem is a nail, not every DB is a hammer. Know when to pick each.

⥽ CAP Theorem & Consistency Models
> Distributed systems fail in surprising ways. CAP and consistency are what separate coders from engineers.

⥽ CDN & Edge Computing
> Speed isn’t just about code. If your users are global, your infra better be too.

⥽ Security Basics
> Learn OAuth, JWTs, and encryption because you don’t want to be the engineer who lets a breach happen.

⥽ CI/CD & Git
> Automated tests, clean deployments, and rollback plans.
AI can’t fix a botched deploy for you.

Write some scripts, push your local hardware, break things, and figure out why. This is how you build instincts that AI can’t teach.

AI will make you faster, but these fundamentals make you effective and productive.

#############################