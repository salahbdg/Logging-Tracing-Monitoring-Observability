# Logging Tracing Monitoring Observability for doodle

In this project, we will perform logging, tracing, monitoring and observability for doodle, a microservices based web app

Here is a diagram to visualize the workflow

```mermaid
graph TD
    subgraph Quarkus Microservices
        A[Login Service] -->|Tracing| B(OpenTelemetry)
        A -->|Metrics| C(Micrometer)
        A -->|Logging| D(SLF4J / Quarkus Logging)
        A -->|Health Checks| E(SmallRye Health)
    end

    B --> F[Jaeger]
    B --> G[Grafana Tempo]

    C --> H[Prometheus]
    H --> I[Grafana]

    D --> J[ELK Stack or Loki]
    J --> I

    F --> I
    G --> I

    E --> I

    style A fill:#f9f,stroke:#333,stroke-width:1px
    style I fill:#bbf,stroke:#333,stroke-width:1px


```


## Logging



## Tracing



## Monitoring



## Observability