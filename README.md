# Secure Web Infrastructure Deployment on AWS (EC2 & VPC)

This project covers the design, configuration, and implementation of a secure cloud infrastructure for the institutional website of the **Vida Plena Barcelona** community. The environment was built following networking, security, and Linux administration best practices to ensure high availability and strict financial governance.

---

## 🛠️ Tech Stack & AWS Services
*   **Cloud Provider:** AWS (Amazon Web Services)
*   **Networking & Security:** AWS VPC, Public Subnets, Security Groups (Firewalls)
*   **Compute & OS:** Amazon EC2 (Ubuntu Server Instance)
*   **Web Server:** Nginx (Reverse Proxy & Web Server configuration)
*   **Monitoring & Observability:** Amazon CloudWatch (Infrastructure Metrics)
*   **Domain & DNS Management:** Amazon Route 53 & Namecheap
*   **Governance & Cost Optimization:** AWS Budgets (Cost Alarms)

---

## 📐 Network Architecture & Infrastructure

The project is structured around a traditional multi-layer production architecture:

1.  **Virtual Private Cloud (VPC):** Designed an isolated network segment within the AWS region to host resources securely.
2.  **Perimeter Security (Security Groups):** Configured strict firewall rules at the instance level, allowing only necessary inbound web traffic (HTTP Port 80 / HTTPS Port 443) and restricted administrative remote access (SSH Port 22).
3.  **Application Server (EC2):** Deployed an **Ubuntu Server** instance, optimized to handle production workloads.
4.  **Web Server Deployment (Nginx):** Installed and configured **Nginx** inside the Ubuntu environment to securely serve the web assets, manage incoming HTTP traffic, and handle routing efficiently.
5.  **Monitoring & Observability:** Integrated **Amazon CloudWatch** to track infrastructure behavior, resource utilization, and operational health, ensuring data-driven insight into the server's performance.
6.  **Production Routing & DNS:** Linked the production domain `vidaplenabarcelona.com` (managed in Namecheap) with an **Amazon Route 53** Hosted Zone, enabling global name resolution to the server's public IP address.

<img width="1365" height="630" alt="Captura desde 2026-06-25 21-36-56" src="https://github.com/user-attachments/assets/d4afb99f-bc6d-4e01-abbe-bcb78b093ecc" />

---

## 📊 Financial Governance & Cost Audit (FinOps)

As part of a Cloud Engineer's core responsibilities, this environment features active financial monitoring to prevent budget overruns and optimize infrastructure spend:

### 1. Budget Control (AWS Budgets & CloudWatch Alarms)
Automated cost tracking and metrics have been implemented to instantly notify when forecasted or actual usage exceeds established thresholds, ensuring total governance over the AWS account.

<img width="1365" height="630" alt="Captura desde 2026-06-25 21-48-40" src="https://github.com/user-attachments/assets/206c3193-15ed-4375-8e38-52f1d70adc4a" />

### 2. Actual Billing Analysis
During the latest infrastructure cost audit, fixed costs derived from the environment architecture were identified and analyzed:

| AWS Service | Cost Component / Reason | Free Tier Status |
| :--- | :--- | :--- |
| **Amazon Route 53** | Active DNS Hosted Zone management for internet routing. | Fixed cost by design ($0.50/month). |
| **AWS VPC / EC2** | Public IPv4 address allocation associated with the web server. | Global standard network charge per active IP hour. |

<img width="1331" height="621" alt="Captura desde 2026-06-25 22-09-53" src="https://github.com/user-attachments/assets/094f85c3-5f4b-4b3a-8255-0294abce435c" />


---

## 🚀 Project Conclusions
This lab simulates a real-world production environment. It demonstrates not only the technical capability to provision servers, configure web applications with Nginx, monitor health, and link live internet domains, but also the professional maturity required to audit cloud costs, report expenditures, and protect a client's financial infrastructure.
