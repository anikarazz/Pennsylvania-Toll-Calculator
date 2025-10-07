# Pennsylvania Toll Calculator (AWS Cloud Application)

A serverless toll calculator web application built for **Cloud Architecture (MIS 3502)**

This project leverages **AWS Lambda**, **API Gateway**, and **RDS (MySQL)** to calculate tolls dynamically based on entry and exit interchanges along the Pennsylvania Turnpike.

The goal was to design and deploy a **scalable, serverless cloud application** that replicates the toll calculation system for the Pennsylvania Turnpike. The system retrieves interchange data, calculates tolls, and returns results through REST APIs, all powered by AWS services.

(Bonus: handles 4× higher traffic — the network kind, not the car kind 💻🚗)

---

**Key AWS Services Used**
- AWS Lambda (Node.js)
- Amazon API Gateway
- Amazon RDS (MySQL)
- EC2 instance (for database hosting)
- IAM Roles & Lambda Layers
- Amazon VPC, Security Groups, Auto Scaling, and Load Balancer

---

## Architecture

The application follows a RESTful architecture designed around AWS-managed services:

1. **Frontend (HTML/JavaScript):** Collects user input for entry and exit points.
2. **API Gateway:** Exposes endpoints for toll calculation and interchange data retrieval.
3. **AWS Lambda Functions:**
   - `GetToll`: Calculates total toll based on selected interchanges.
   - `GetInterchange`: Retrieves entry and exit data from the MySQL database.
4. **Amazon RDS (MySQL):** Stores toll rates, interchange data, and distance information.
5. **VPC & Load Balancer:** Ensures secure networking and scalability for backend resources.

---

❗️ Please note: Due to the expiration of my AWS Free Tier account after the semester ended, the live Lambda functions, API Gateway endpoints, and RDS database are no longer active.
As a result, this repository contains screenshots and documentation of the original implementation instead of runnable code.
