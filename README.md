# Pan-African E-Commerce Cloud Architecture 🌍

## Project Overview
This repository contains the architectural design for a high-availability, low-latency e-commerce portal tailored for the African market. The design prioritizes cost-efficiency ("low budget") while addressing strict constraints regarding latency, security, and fault tolerance.

## 📂 Deliverables
- **[Architectural Diagram](diagrams/architecture_diagram.png)**
- **[Implementation Document](docs/implementation_strategy.md)**

## 🏗 Architecture Highlights

### 1. Solving for Latency (The Africa Constraint)
To address the requirement for "very low-latency" in the African region:
- **CloudFront (CDN):** Deployed to cache static assets (product images) at edge locations closer to the user (e.g., Cape Town, Lagos, Nairobi).

### 2. Cost & Fault Tolerance
To meet the "low budget" and "fault tolerant" requirements:
- **Auto Scaling Group:** Dynamic scaling ensures we only pay for compute capacity when needed.
- **Application Load Balancer:** Distributes traffic and handles SSL termination for security in transit.

### 3. Data Strategy
- **S3 (Object Storage):** Used for "storing pictures for products" to reduce database load and storage costs.
- **RDS Multi-AZ:** Stores user relational data with a standby replica for high availability.

## 🛠 Tools Used
- **Architecture Design:** [draw.io](https://draw.io)
- **Documentation:** Markdown & PDF

---
*Designed as part of the Cloud Squad Architecture Challenge.*
