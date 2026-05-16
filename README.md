# Centralized Logging with Loki + Grafana

Production-grade centralized logging stack using Grafana Loki, Promtail and Grafana.

## What it does
- Promtail collects logs from system and Docker containers automatically
- Loki stores and indexes logs efficiently with minimal resources
- Grafana visualizes and searches logs in real time

## Why Loki over ELK
- 10x lighter than Elasticsearch
- No full-text indexing — uses labels instead
- Native Grafana integration
- Perfect for teams already using Prometheus and Grafana

## Stack
- Grafana Loki 2.9.0
- Promtail 2.9.0
- Grafana (latest)
- Docker Compose

## Usage
docker compose up -d

Then open Grafana at http://localhost:3000
- Login: admin / admin
- Add Loki data source: http://loki:3100
- Go to Explore and select job=varlogs to see system logs

## Destroy
docker compose down# elk-stack-logging
