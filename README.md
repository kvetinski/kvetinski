# Anton Kvetinski

### Senior Backend & Distributed Systems Engineer

**Go · Rust · Distributed Systems**

I build backend and distributed systems that remain understandable under pressure. My production background spans fintech, betting, crypto trading, and supply-chain platforms, with a focus on concurrency, transaction correctness, failure isolation, observability, and performance.

My current public work applies that experience to Rust and Go systems projects with explicit trade-offs, reproducible evidence, and documented limitations.

## Selected production impact

- Reduced average request latency by **35%** by profiling and optimizing concurrent request paths in distributed supply-chain services processing **10,000+ orders/day**.
- Designed and scaled Go services for real-time betting infrastructure sustaining peak traffic of **~8,000 requests/second**.
- Built Go backend infrastructure for a cryptocurrency futures platform handling **~1,000 requests/second**.

## Selected systems work

### [Pulse](https://github.com/kvetinski/pulse) — distributed gRPC scenario engine

An experimental Rust/Tokio runtime for scenario-driven gRPC load execution. Pulse explores scheduler/worker separation, Kafka job distribution, Redis-backed coordination, dynamic descriptor-driven unary calls, bounded queues, retry/DLQ paths, and Prometheus metrics.

The repository includes architecture decisions, Kubernetes manifests, reliability tests, runbooks, SLO/alerting guidance, and explicit failure-boundary limitations.

[Architecture decisions](https://github.com/kvetinski/pulse/tree/master/docs/adr) · [Operational safety](https://github.com/kvetinski/pulse/blob/master/docs/operational-safety.md) · [Known limitations](https://github.com/kvetinski/pulse#known-limitations--caveats)

### [LineRate](https://github.com/kvetinski/line_rate) — Go/Rust performance investigation

A Linux-first performance lab that evolves one large-file IPv4 workload from buffered I/O through `mmap`, zero-allocation parsing, atomics, and worker-local data structures in both Go and Rust.

The central question is not “which language wins?” It is how workload cardinality, memory traffic, synchronization, and cache behavior change the right design.

[Lessons](https://github.com/kvetinski/line_rate/tree/master/lessons) · [Benchmark methodology](https://github.com/kvetinski/line_rate/blob/master/docs/benchmark_methodology.md) · [Result provenance](https://github.com/kvetinski/line_rate/blob/master/results/curated/metadata.md)

## Engineering approach

> Bound the work. Define the failure semantics. Instrument the system. Measure before optimizing.

- Prefer bounded concurrency and explicit backpressure over hidden queue growth.
- Treat retries as additional load and define their idempotency and commit boundaries.
- Use representative workloads and retain enough evidence to reproduce performance conclusions.
- Treat metrics, traces, dashboards, alerts, runbooks, and limitations as part of the system design.

## Core technologies

- **Languages and runtime:** Go, Rust, Tokio
- **Services and data:** gRPC, REST, Kafka, NATS, Redis, PostgreSQL, ClickHouse
- **Platform and observability:** Kubernetes, Docker, Prometheus, Grafana, OpenTelemetry

## Contact

Open to backend, distributed-systems, and infrastructure roles — remote or relocation.

[LinkedIn](https://www.linkedin.com/in/antonkvetinski/) · [Email](mailto:anton.kvetinski13@gmail.com)
