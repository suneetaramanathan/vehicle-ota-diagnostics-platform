# Vehicle OTA Update & Remote Diagnostics Platform

> 🚧 **Status: In progress (started November 2026)**

A Java / Spring Boot backend that simulates how connected vehicles receive **Over-the-Air (OTA) software updates** and send **telemetry and diagnostic data** to the cloud (offboard diagnostics).

I'm building this project to deepen my skills in automotive backend engineering, combining my B.Tech in Electronics & Communication Engineering with my experience in data engineering and cloud deployment.

---

## 🎯 Goals

- Manage firmware packages with **versioning** and target vehicle models
- Run **staged OTA rollouts** (e.g. 10% of the fleet first, then 100%)
- **Verify updates securely** with SHA-256 checksums and digital signatures
- Collect **vehicle telemetry** (speed, battery, temperature) and **fault codes (DTCs)**
- Detect faults and raise alerts (offboard diagnostics)
- Simulate a fleet of vehicles that check for updates and report status

## 🛠️ Tech Stack

| Area | Technologies |
|------|--------------|
| Language | Java 17 |
| Framework | Spring Boot, Spring Web, Spring Data JPA |
| Database | PostgreSQL |
| Testing | JUnit 5, integration tests |
| Build | Maven |
| DevOps | Docker, docker-compose, GitHub Actions |
| Planned | Kubernetes (minikube), Spring Security / JWT, API Gateway |

## 🔌 Planned REST Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/firmware` | Upload a new firmware package (version, model, checksum) |
| GET | `/api/firmware/{id}` | Get firmware details |
| POST | `/api/campaigns` | Create an OTA rollout campaign |
| GET | `/api/vehicles/{vin}/updates` | Vehicle checks for an available update |
| POST | `/api/vehicles/{vin}/updates/status` | Vehicle reports update success / failure |
| POST | `/api/telemetry` | Vehicle sends telemetry data |
| POST | `/api/diagnostics/dtc` | Vehicle reports a fault code |
| GET | `/api/diagnostics/alerts` | List active diagnostic alerts |

## 🗺️ Roadmap

- [ ] **Phase 1:** OTA Update Service: firmware upload, versioning, update check API
- [ ] **Phase 2:** Vehicle Simulator: virtual fleet polling for updates and sending telemetry
- [ ] **Phase 3:** Diagnostics Service: telemetry storage, DTC processing, alert rules
- [ ] **Phase 4:** Secure updates: SHA-256 checksum and signature verification
- [ ] **Phase 5:** Docker, docker-compose and GitHub Actions CI (JUnit tests)
- [ ] **Phase 6:** Kubernetes deployment, JWT security and API gateway
- [ ] **Phase 7:** Diagnostics dashboard (Power BI / web)

## 👩‍💻 Author

**Suneeta Ramanathan**
B.Tech Electronics & Communication Engineering | MSc Business Analytics & Data Science
Munich, Germany · [LinkedIn](https://www.linkedin.com/in/suneeta-ramanathan)
