# Hi, I'm Anton Kvetinski

**I turn unstable distributed systems into predictable platforms through concurrency control, backpressure, and production visibility.**

![Go](https://img.shields.io/badge/Go-production_backend-00ADD8?style=flat-square\&logo=go\&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-systems_engineering-000000?style=flat-square\&logo=rust\&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-event_driven_systems-231F20?style=flat-square\&logo=apachekafka\&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-platform_ops-326CE5?style=flat-square\&logo=kubernetes\&logoColor=white)
![Reliability](https://img.shields.io/badge/Focus-reliability_under_load-brightgreen?style=flat-square)

I’m a backend and systems engineer with 6+ years building high-load infrastructure across fintech, betting, crypto, trading, and supply-chain systems.

My production background is mostly in **Go distributed systems**. My current technical direction is deeper **systems engineering with Rust**: async runtimes, service coordination, backpressure, and predictable behavior under load.

---

## ⚙️ My engineering philosophy

When I design or review a service, I ask:

* What happens when traffic spikes?
* Can queues grow without bound?
* Are retries safe, or can they amplify failure?
* Are operations idempotent?
* Can we debug the system from metrics, logs, and traces?
* What happens when Redis, Kafka, PostgreSQL, or another dependency becomes slow?
* Is latency predictable, or only acceptable in the happy path?

I use backpressure, bounded concurrency, idempotency, circuit breakers, retries with clear boundaries, DLQ behavior, and distributed tracing as practical guards against production instability.

For critical services, I also care about the operational layer: metrics, dashboards, alerts, runbooks, deployment notes, and documented limitations.

If a system cannot be debugged in production, it is not really finished.

---

## 🚀 Selected systems work

### [Pulse](https://github.com/kvetinski/pulse) — Distributed gRPC load engine in Rust

I wanted a load engine that behaved more like production infrastructure: controlled concurrency, backpressure, coordination, metrics, and explicit failure documentation — not just a script that fires requests.

Pulse is a Tokio-based distributed runtime for scenario-based gRPC load execution.

**What it does:**

* Scheduler/worker architecture
* Kafka job distribution
* Redis leader election and idempotency
* Bounded queues and backpressure
* Dynamic gRPC calls from descriptor sets
* Request templating and per-step metrics
* Kubernetes manifests, runbooks, SLO/alerting docs, rollout notes, and documented limitations

**Design note:**

I chose bounded channels over unbounded queues because a load engine should expose pressure, not hide it.

Unbounded queues can make a system look healthy while memory grows and latency becomes unstable. Bounded queues force the runtime to reveal its limits early, which is exactly what I want when testing distributed systems under stress.

Pulse is not a syntax demo. It is a distributed infrastructure project where runtime behavior, failure modes, and operational review are the point.

---

### [Account Service](https://github.com/kvetinski/account) — Production-style Go backend service

A Go backend service showing how I structure service boundaries, observability, and deployment readiness before applying the same patterns to financial or reliability-critical systems.

It demonstrates:

* Layered Go backend architecture
* gRPC service interface
* PostgreSQL persistence
* OpenTelemetry tracing
* Prometheus/Grafana metrics
* Jaeger tracing
* Kubernetes deployment
* Integration testing

The goal is to show backend code as an operable service, not just a collection of handlers.

---

## 🧰 Technical stack

`Go` · `Rust` · `TypeScript`
`gRPC` · `REST` · `GraphQL`
`Kafka` · `NATS` · `Redis`
`PostgreSQL` · `ClickHouse` · `MongoDB`
`Kubernetes` · `Docker`
`Prometheus` · `Grafana` · `OpenTelemetry` · `Jaeger`
`backpressure` · `idempotency` · `retries` · `DLQ` · `circuit breakers` · `profiling`

---

## 🎯 What I’m looking for

I’m focused on backend and systems roles where reliability, concurrency, observability, and performance matter.

The work I want more of:

* Distributed infrastructure
* Backend platform engineering
* Rust / Go systems engineering
* Performance-critical services
* Reliability-sensitive fintech, trading, cloud, security, robotics, or infrastructure systems

I’m strongest when I can make high-load backend systems easier to reason about, operate, and debug.

---

## 📫 Let’s connect

I’m always open to discussing distributed systems, Rust/Go trade-offs, production debugging, reliability, or performance engineering.

* LinkedIn: [linkedin.com/in/antonkvetinski](https://www.linkedin.com/in/antonkvetinski/)
* GitHub: [github.com/kvetinski](https://github.com/kvetinski)
* Email: [anton.kvetinski13@gmail.com](mailto:anton.kvetinski13@gmail.com)
