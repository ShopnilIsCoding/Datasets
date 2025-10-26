# Synthetic Certificate Lifecycle Dataset

This repository contains a synthetic dataset generated for research on **Automated Certificate and API Security Lifecycle Management**. The dataset simulates real-world scenarios of certificate usage across distributed API-based systems, including normal and misuse behavior.

---

## 📄 Dataset Description

The dataset file:

synthetic_certificate_lifecycle.csv


contains simulated certificate events with lifecycle information. Each row represents a certificate associated with an API endpoint and includes metadata useful for modeling certificate compliance, anomaly detection, and security monitoring.

---

## 📊 File Structure

| Column Name              | Description |
|-------------------------|-------------|
| certificate_id          | Unique identifier for each certificate |
| domain                  | Domain or API endpoint using the certificate |
| issue_date              | Certificate issuance date |
| expiry_date             | Certificate expiration date |
| status                  | Current certificate status (`valid`, `expired`, `revoked`) |
| key_length              | Public key length (e.g. 2048, 4096) |
| signature_algorithm     | Digital signature algorithm used |
| issuer                  | Certificate Authority (CA) issuing the certificate |
| usage_context           | Certificate usage scenario (API/server/microservice) |
| security_score          | Security risk score (synthetic metric) |

> **Note:** The dataset is synthetic and does not contain sensitive or real security data.

---

## ✅ Use Cases

This dataset is designed for academic and security research, including:

- Certificate misuse detection  
- TLS compliance analysis  
- API security modeling  
- Anomaly detection in certificate behavior  
- Machine learning experiments in cybersecurity  

---

## 🔧 Example Usage

```python
import pandas as pd

# Load dataset
df = pd.read_csv("synthetic_certificate_lifecycle.csv")

# View basic statistics
print(df.head())
print(df['status'].value_counts())
