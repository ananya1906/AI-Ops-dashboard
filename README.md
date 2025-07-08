# AI Ops Monitoring Dashboard

This project demonstrates a complete DevOps-style monitoring setup for a Node.js application. It uses Prometheus to scrape performance metrics and Grafana to visualize them in real time. All services are containerized and orchestrated using Docker Compose.

The goal is to simulate a real-world observability and monitoring pipeline—commonly used in DevOps and AIOps environments—to track system health, performance, and reliability.

---

## Features

- Node.js service that exposes runtime metrics (CPU, memory, event loop lag)
- Prometheus collects metrics at regular intervals from the service
- Grafana displays real-time performance data through customizable dashboards
- Docker Compose manages and runs the entire stack locally

---

## Technology Stack

- Node.js (Express) for the sample service
- prom-client for exporting metrics
- Prometheus for metrics scraping and storage
- Grafana for dashboard and visualization
- Docker and Docker Compose for container orchestration

---

## Project Structure

ai-ops-dashboard/
├── node-service/ # Node.js metrics service
│ ├── server.js
│ ├── package.json
│ └── Dockerfile
├── prometheus/ # Prometheus configuration
│ └── prometheus.yml
├── docker-compose.yml # Main orchestration file
└── README.md




