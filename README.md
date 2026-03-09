# Software Construction Research: Microservices

## Introduction
Modern software systems are becoming increasingly complex. To manage this complexity, many companies adopt **Microservices Architecture**. Microservices break a large application into smaller independent services. Each service performs a specific function and communicates with other services through APIs.

This approach allows companies to scale systems easily, update components independently, and improve reliability. However, microservices can also introduce complexity, which has caused some companies to move back to a **monolithic architecture**.

This research looks at:
1. How Netflix uses microservices.
2. Other companies successfully using microservices.
3. Companies that moved away from microservices back to monolithic systems.

---

# 1. How Netflix Uses Microservices

Netflix is one of the most famous examples of a company that successfully uses **microservices architecture**.

Originally, Netflix used a **monolithic system**, but as the platform grew and the number of users increased, the system became difficult to scale and maintain. Netflix therefore migrated to a **microservices architecture hosted on the cloud (AWS)**.

Instead of one large application, Netflix now runs **hundreds of small services**, each responsible for a specific task such as:

- User authentication
- Video streaming
- Recommendations
- Search
- Billing
- Content delivery

Each service can be developed, deployed, and scaled independently.

### Key technologies used by Netflix
Netflix developed several tools to support microservices:

- **Eureka** – service discovery
- **Zuul** – API gateway
- **Hystrix** – fault tolerance
- **Ribbon** – load balancing
- **Chaos Monkey** – failure testing

### Benefits Netflix gets from microservices
- Independent deployment of services
- Better scalability
- Faster innovation
- Higher system reliability
- Fault isolation (failure in one service does not crash the entire system)

Because of these advantages, Netflix can support **millions of users streaming simultaneously worldwide**.

---

# 2. Other Companies Using Microservices

Many large technology companies use microservices successfully.

## Uber
Uber originally started with a **monolithic architecture**, but as the company expanded globally, the system became difficult to manage.

Uber adopted microservices so that different teams could manage different parts of the system independently.

Today Uber operates **thousands of microservices** supporting services such as:

- Ride requests
- Driver management
- Payment processing
- Maps and navigation
- Uber Eats

Microservices allow Uber to scale specific services depending on demand in different regions.

### Benefits for Uber
- Independent scaling of services
- Faster deployment
- Support for global operations
- Improved reliability

---

## Spotify
Spotify uses microservices to manage its music streaming platform.

Spotify organizes teams into **small autonomous teams called "squads"**. Each squad is responsible for a specific microservice.

Examples of Spotify services include:

- Music recommendations
- User playlists
- Search
- Streaming
- User accounts

Spotify also built an internal developer platform called **Backstage**, which helps engineers easily create and manage microservices.

### Benefits for Spotify
- Faster feature development
- Independent team ownership
- Continuous deployment
- Scalability for millions of users

---

# 3. Companies That Moved Back From Microservices

Although microservices offer many advantages, some companies discovered that they introduced **too much complexity**. As a result, some organizations moved back to **monolithic or modular monolithic architectures**.

## Segment

Segment is a **Customer Data Platform (CDP)** that helps companies collect user data from websites and applications and send it to analytics and marketing tools.

Segment originally built its system using **over 100 microservices**. Each service handled a small part of the system.

However, managing so many services became extremely difficult. Engineers had to deal with:

- Service communication
- Multiple deployments
- Complex debugging
- Distributed monitoring

Because of these challenges, Segment decided to **combine many services into a monolithic architecture**.

### Results
After moving back to a monolith:
- Development became faster
- Maintenance became easier
- System complexity was reduced

### Reasons for the change
- Too many services to manage
- Deployment complexity
- Difficult debugging
- Lower developer productivity

---

## Amazon Prime Video

Amazon Prime Video also experienced issues with microservices in one of its internal systems.

The company originally built a monitoring system using multiple microservices. Each service processed and transferred data to other services.

However, this architecture created excessive **data transfer between services**, which significantly increased infrastructure costs.

Amazon engineers redesigned the system and replaced the microservices with a **single monolithic service** for that particular workflow.

### Results
After the redesign:
- Infrastructure costs were reduced by **about 90%**
- System performance improved
- Architecture became simpler

### Reasons for the change
- High operational cost
- Excessive service communication
- Unnecessary system complexity

---

## Others

Several other well-known companies have also reduced or reconsidered microservices:

- **InVision** – merged several services back into a monolith to reduce infrastructure costs.
- **Shopify** – adopted a **modular monolith** instead of fully distributed microservices.
- **Basecamp (37signals)** – chose a monolithic architecture for simplicity and easier development.
- **SoundCloud** – simplified its architecture after managing too many microservices became difficult.
- **Etsy** – restructured parts of its architecture to reduce distributed system complexity.

---

# Conclusion

Microservices architecture is very powerful for large-scale systems. Companies like **Netflix, Uber, and Spotify** use microservices successfully to support millions of users and scale their platforms globally.

However, microservices are not always the best solution. Some companies such as **Segment and Amazon Prime Video** discovered that microservices introduced unnecessary complexity and cost. These companies simplified their systems by returning to monolithic or modular architectures.

This shows that the best architecture depends on the **size of the company, system requirements, and team capabilities**.
