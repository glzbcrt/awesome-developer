# Observability

## Platforms and Tools

- [Sentry](https://sentry.io)
- [Vector by Datadog](https://vector.dev/)

## Aspire

- [Aspire dashboard overview](https://learn.microsoft.com/en-us/dotnet/aspire/fundamentals/dashboard/overview?tabs=bash)
- [Aspire telemetry](https://learn.microsoft.com/en-us/dotnet/aspire/fundamentals/telemetry)

## Structured/Semantic Logging

- [Message Templates](https://messagetemplates.org/)
- [How to use structured logging](https://github.com/NLog/NLog/wiki/How-to-use-structured-logging)

## Metrics

- [A Deep Dive Into the Four Types of Prometheus Metrics](https://www.tigerdata.com/blog/four-types-prometheus-metrics-to-collect)
- [A Deep Dive Into OpenTelemetry Metrics](https://www.tigerdata.com/blog/a-deep-dive-into-open-telemetry-metrics)
- [Prometheus vs. OpenTelemetry Metrics: A Complete Guide](https://www.tigerdata.com/blog/prometheus-vs-opentelemetry-metrics-a-complete-guide)

## OpenTelemetry

- [OTLP Specification 1.8.0](https://opentelemetry.io/docs/specs/otlp/)
- [OpenTelemetry Protocol (OTLP): A Deep Dive into Observability](https://last9.io/blog/opentelemetry-protocol-otlp/)
- [OpenTelemetry Protocol (OTLP) Specification](https://github.com/open-telemetry/opentelemetry-proto)
- [Tracing API](https://opentelemetry.io/docs/specs/otel/trace/api/)

- [OpenTelemetry Demo](https://opentelemetry.io/docs/demo/architecture/)
- [OpenTelemetry Demo GitHub repo](https://github.com/open-telemetry/opentelemetry-demo)

- [Distributions](https://opentelemetry.io/docs/concepts/distributions/)
- [Building your own OpenTelemetry Collector distribution](https://medium.com/opentelemetry/building-your-own-opentelemetry-collector-distribution-42337e994b63)

- [HTTP semantic conventions declared stable](https://opentelemetry.io/blog/2023/http-conventions-declared-stable/)

### Azure

- [Announcing Azure Monitor OpenTelemetry Distro](https://devblogs.microsoft.com/dotnet/azure-monitor-opentelemetry-distro/#open-and-extensible-design)
- [Making Azure the Best Place to Observe Your Apps with OpenTelemetry](https://techcommunity.microsoft.com/blog/azureobservabilityblog/making-azure-the-best-place-to-observe-your-apps-with-opentelemetry/3995896)

### Collector

- [OpenTelemetry Collector GitHub repo](https://github.com/open-telemetry/opentelemetry-collector)
- [OpenTelemetry Collector Contrib GitHub repo](https://github.com/open-telemetry/opentelemetry-collector-contrib)
- [Architecture](https://opentelemetry.io/docs/collector/architecture/)
- [Configuration](https://opentelemetry.io/docs/collector/configuration/)
- [OpenTelemetry Protocol Exporter](https://opentelemetry.io/docs/specs/otel/protocol/exporter/)
- [Troubleshooting](https://opentelemetry.io/docs/collector/troubleshooting/)
- [OTLP Exporter Configuration](https://opentelemetry.io/docs/languages/sdk-configuration/otlp-exporter/)

- [File Log Receiver](https://github.com/open-telemetry/opentelemetry-collector-contrib/tree/main/receiver/filelogreceiver)
- [Windows Event Log Receiver](https://github.com/open-telemetry/opentelemetry-collector-contrib/tree/main/receiver/windowseventlogreceiver)

- [Host Metrics Receiver](https://github.com/open-telemetry/opentelemetry-collector-contrib/tree/main/receiver/hostmetricsreceiver)
- [OpenTelemetry Host Metrics receiver](https://uptrace.dev/opentelemetry/collector/host-metrics)

- [So You Built A Custom Collector with the OpenTelemetry Collector Builder…Now What?](https://medium.com/womenintechnology/so-you-built-a-custom-collector-with-the-opentelemetry-collector-builder-now-what-6588952ee6c5)
- [Building a custom collector](https://opentelemetry.io/docs/collector/custom-collector/)
- [OpenTelemetry Collector Builder (ocb)](https://github.com/open-telemetry/opentelemetry-collector/tree/main/cmd/builder)

### SDKs

#### Python

- [Python Guide](https://opentelemetry.io/docs/languages/python/getting-started/)
- [OpenTelemetry Python SDK](https://github.com/open-telemetry/opentelemetry-python)
- [OpenTelemetry-Python-Contrib](https://opentelemetry-python-contrib.readthedocs.io/)

### Tools

- [SigNoz](https://github.com/SigNoz/signoz)

### Semantic Conventions

- [OpenTelemetry Semantic Conventions](https://github.com/open-telemetry/semantic-conventions)
- [Semantic Conventions for HTTP](https://github.com/open-telemetry/semantic-conventions/blob/main/docs/http/http-spans.md)

### Articles

- [Traces and spans](https://cloud.google.com/trace/docs/traces-and-spans)
- [Trace context](https://cloud.google.com/trace/docs/trace-context)
- [Understanding OpenTelemetry - Trace ID vs. Span ID](https://signoz.io/comparisons/opentelemetry-trace-id-vs-span-id/)
- [Understanding Distributed Tracing with a Message Bus](https://www.honeycomb.io/blog/understanding-distributed-tracing-message-bus)

### Wireshark

- [Analyzing gRPC messages using Wireshark](https://grpc.io/blog/wireshark/)
- [Using Wireshark To Analyze The GRPC/ProtoBuf Messages](https://weinan.io/2023/06/20/wireshark.html)
