# Enterprise Observability Platform

A Spring Boot 3 / Java 21 observability sample integrating Elasticsearch 9, Logstash and Kibana. Includes structured application logging, Actuator metrics, Docker Compose, demo traffic, tests, dashboard import starter, and documented alert/notification setup.

## Stack
- Spring Boot 3.5.7, Java 21
- Elasticsearch, Logstash and Kibana 9.2.0
- Docker Compose
- Logback JSON logging, Spring Boot Actuator and Micrometer Prometheus

## Quick start
```bash
cp .env.example .env
docker compose up --build -d
chmod +x scripts/*.sh
./scripts/generate-demo-traffic.sh
```

Open Spring Boot at http://localhost:8080, Elasticsearch at http://localhost:9200 and Kibana at http://localhost:5601.

## Important
This Compose profile is for local development only; Elasticsearch security is disabled. Before production use, enable authentication and TLS, configure secrets, persistence/backup, retention, resource limits, monitoring and multi-node deployment. Kibana alert rules and email/webhook connectors are documented setup instructions and must be configured in Kibana. The saved dashboard is a starter import; create Lens panels as described in `dashboards/README.md`.
