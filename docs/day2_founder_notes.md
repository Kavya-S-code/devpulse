📘 DevPulse – Day 2: MVP Definition & Architecture

Minimum Viable Product
Goal: Define the smallest, most impactful version of DevPulse you can build and demo.

🎯 Core MVP Features
Metrics Dashboard: CPU, memory, request rate, error rate

Plug-and-Play Agent: Auto-integrates with Spring Boot/Quarkus apps

Alerting System: Threshold-based alerts via email/webhook

Config File: YAML/properties-based setup

Minimal UI: Clean dashboard with real-time updates

🚫 Excluded (for now)
Distributed tracing

Multi-tenant support

Role-based access control

Advanced anomaly detection

🧪 Success Criteria
Works with a sample Spring Boot app

Shows live metrics within 5 minutes of setup

Fires alerts when thresholds are breached

Runs locally with Docker

🧠 System Diagram

Spring Boot App → DevPulse Agent → Metrics Collector → Backend Processor → Dashboard UI → Alerting Engine

📝 Raw Thoughts
Choosing metrics + alerts as MVP because they deliver instant value. Tracing/logs can wait.
Using Docker for local dev, VS Code for speed. Will build collector first, then UI.
start coding metrics ingestion + sample config.

⚙️ Draft Config Format

app_name: my-service
metrics:
  cpu: true
  memory: true
  request_rate: true
alerts:
  cpu_threshold: 80
  memory_threshold: 75
  error_rate_threshold: 5
notifications:
  email: abc@company.com
  webhook: https://hooks.devpulse.io/alert


