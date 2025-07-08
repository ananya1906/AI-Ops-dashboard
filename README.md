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

![image](https://github.com/user-attachments/assets/a8affd8b-2535-4d3e-9b0f-ebb2693e792f)


---


### 1. Clone the repository

```bash
git clone https://github.com/ananya1906/ai-ops-dashboard.git
cd ai-ops-dashboard

````
### 2. Start the stack
```bash
docker-compose up --build
```
### Accessing the Services
Node.js metrics: [http://localhost:3000/metrics](url)

Prometheus UI: http://localhost:9090

Grafana UI: http://localhost:3001

Grafana login:
Username: admin

Password: admin
(You will be prompted to change the password on first login.)

### Configurations
Prometheus
Prometheus is configured via prometheus.yml to scrape metrics from the Node.js service:

scrape_configs:
  - job_name: 'node-service'
    static_configs:
      - targets: ['node-service:3000']
   
### Grafana
Once logged in:

1. Add Prometheus as a new data source (URL: http://prometheus:9090)

2. Create a dashboard with panels using queries such as:

- process_cpu_seconds_total

- process_resident_memory_bytes

- nodejs_eventloop_lag_seconds

These queries reflect real-time CPU usage, memory consumption, and event loop performance of the Node.js service.

### Conclusion

This project replicates the foundational infrastructure of AIOps (Artificial Intelligence for IT Operations). Although it doesn't yet include AI/ML models, it demonstrates how operational data is collected and centralized for real-time analysis. The system can be easily extended to add automated alerts, anomaly detection, or predictive analytics.



   








