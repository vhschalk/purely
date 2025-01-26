# PURE: A Platform for Understanding and Relationship Exchange
PURE (Platform for Understanding and Relationship Exchange) is an exploratory system that enriches real-time and batch data with semantic meaning, driving rapid insights across multiple disciplines.

## Requirements
* The primary thesis is to prove that multidisciplinary data from multiple sources can generate more significant insights!
* A generic architectural stack that the system can be deployed on-premises or in the cloud to support any data and privacy policy.
* Only use independent and open-source AI models.
* The system should be able to operate entirely independently, meaning that storage, networking, monitoring, etc., should be provided.
* Be open to changing technology choices and replacing any system as development progresses.
* Generate understanding and relationships with a high level of detail but simplify the system's data ingestion and movement mechanisms.
* Have a central system to manage all internal systems and provide a visual interface and API for configuration and viewing results.
* The central system should use a compiled language with multi-language interface support.

## Licence

GNU AGPLv3

## Core technology choices

| #  | Technology                     | Purpose                                                                                                                                      | License                                                 |
|----|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| 1  | ASP.NET Core                   | Cross-platform framework for building backend APIs and web applications in C#                                                                | MIT                                                     |
| 2  | Kubernetes                     | Orchestrates containerized applications, enabling scalable, reproducible, and fault-tolerant deployments                                     | Apache 2.0                                              |
| 3  | Vespa                          | A search and recommendation engine that combines vector, text, tensor, and structured data processing                                        | Apache 2.0                                              |
| 4  | Sentence Transformers (SBERT)  | Pre-trained NLP models that generate high-quality vector embeddings for semantic search and similarity tasks                                 | Apache 2.0                                              |
| 5  | PostgreSQL                     | An open-source relational database with advanced features like JSON support and strong ACID compliance                                       | PostgreSQL License (similar to MIT)                     |
| 6  | TimescaleDB                    | A PostgreSQL-based time-series database optimized for scalability and analytics on time-series data for both model telemetry and system logs | Timescale License (TSL), Apache 2.0 (community edition) |
| 7  | RabbitMQ                       | A reliable message broker that enables asynchronous communication between services using various messaging protocols                         | MPL 2.0                                                 |
| 8  | MinIO                          | An S3-compatible object storage solution designed for high-performance, scalable cloud storage                                               | AGPL v3 (Apache 2.0 for older versions)                 |
| 9  | Traefik                        | A modern cloud-native reverse proxy and load balancer for routing internal and external traffic                                              | MIT                                                     |
| 10 | Smallstep                      | An internal certificate authority (CA) and identity system for managing TLS certificates and authentication                                  | Apache 2.0                                              |
| 11 | Let's Encrypt                  | A free, automated, and open certificate authority for securing external web services with TLS                                                | ISRG Certificate Policy (open and free use)             |
| 12 | Airbyte                        | Batch data ingestion and ETL for various data sources into PURE                                                                              | ELv2 (Elastic License)                                  |
| 13 | Temporal.io                    | Workflow orchestration and scheduling for handling complex business processes and task dependencies                                          | MIT                                                     |
| 14 | Lucene (NuGet)                 | Full-text search engine for indexing and searching structured/unstructured data                                                              | Apache 2.0                                              |
| 15 | PDFSharp (NuGet)               | PDF document processing library for transformation and manipulation                                                                          | MIT                                                     |
| 16 | Schema.net (NuGet)             | Provides standardized semantic vocabularies for enriching and structuring data                                                               | MIT                                                     |
| 17 | tryAGI.net (NuGet)             | A ML model management library for handling inference and training workflows                                                                  | Apache 2.0                                              |
| 18 | Horizontal Pod Autoscaler (K8) | Auto-scales Kubernetes workloads based on CPU, memory, or custom metrics                                                                     | Apache 2.0                                              |
| 19 | OpenTelemetry Connectors       | Collects and exports telemetry data (traces, metrics, logs) for observability                                                                | Apache 2.0                                              |
| 20 | Prometheus                     | A monitoring system for collecting and querying time-series metrics                                                                          | Apache 2.0                                              |
| 21 | Grafana Tempo                  | Distributed tracing backend for storing and querying traces                                                                                  | AGPL v3                                                 |
| 22 | Grafana                        | Visualization platform for real-time monitoring and dashboards                                                                               | AGPL v3                                                 |

## Future Considerations

| #  | Technology       | Purpose                                                                                                                                         | License               |
|----|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| 1  | Apache Tika      | Multi-format document parsing and metadata extraction (potential replacement for PDFSharp)                                                      | Apache 2.0            |
| 2  | EdgeX Foundry    | Open-source platform to ingress and manage diverse IIoT protocols                                                                               | Apache 2.0            |
| 3  | Apache NiFi      | Batch data ingestion and ETL for various data sources into PURE (potential replacement for Airbyte based on performance and licence evaluation) | Apache 2.0            |
| 4  | Terraform        | Infrastructure as Code (IaC) tool for automating cloud and on-prem resource provisioning                                                        | MPL 2.0               |

## Architecture

The diagram below summarises PURE's system architecture.

![System Architecture](Architecture/Pure_System_Architecture.svg)
