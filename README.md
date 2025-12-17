# Monitoring Stack

Complete monitoring and observability stack for Kubernetes.

## Components

### Prometheus
Metrics collection and storage with alerting capabilities.

### Grafana
Visualization and dashboarding for metrics and logs.
- Access: https://grafana0213.kro.kr

### Loki
Log aggregation system designed for Kubernetes.

### Promtail
Log shipping agent for Loki.

### Alertmanager
Alert routing and notification management.

### kube-state-metrics
Kubernetes cluster state metrics exporter.

### node-exporter
Hardware and OS metrics exporter for nodes.

## Architecture

```
Applications → Prometheus (metrics)
           → Promtail → Loki (logs)

Grafana ← Prometheus (datasource)
        ← Loki (datasource)

Prometheus → Alertmanager (alerts)
```

## Deployment

Managed by ArgoCD. All components are deployed to the `monitoring` namespace.
