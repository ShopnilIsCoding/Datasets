# Synthetic Certificate Lifecycle Dataset

This repository contains a synthetic dataset generated for research on **Automated Certificate and API Security Lifecycle Management**. The dataset simulates real-world scenarios of certificate usage across distributed API-based systems, including both normal operation and misuse conditions such as expired or revoked certificate activity.

---

## Dataset Description

The dataset file included in this repository:

```
synthetic_certificate_lifecycle.csv
```

contains simulated certificate lifecycle events that can be used for machine learning experiments, anomaly detection, and certificate compliance monitoring.

Each row corresponds to one certificate associated with an API endpoint.

---

## File Structure

| Column Name         | Description                                                |
| ------------------- | ---------------------------------------------------------- |
| certificate_id      | Unique identifier for each certificate                     |
| domain              | Domain or API endpoint using the certificate               |
| issue_date          | Certificate issuance date                                  |
| expiry_date         | Certificate expiration date                                |
| status              | Current certificate status (`valid`, `expired`, `revoked`) |
| key_length          | Public key length in bits (e.g. 2048, 4096)                |
| signature_algorithm | Signature algorithm used (e.g. RSA-SHA256)                 |
| issuer              | Certificate authority (CA) that issued the certificate     |
| usage_context       | Usage type (API server, microservice endpoint, etc.)       |
| security_score      | Synthetic security confidence score                        |

> **Note**: This dataset is fully synthetic and safe for academic and industrial experimentation.

---

## Use Cases

This dataset is suitable for:

* Certificate misuse detection
* TLS/SSL lifecycle compliance research
* Security monitoring simulations
* Certificate risk scoring
* Deep learning and anomaly detection experiments
* Cybersecurity automation research

---

## Example Usage

```python
import pandas as pd

# Load dataset
df = pd.read_csv("synthetic_certificate_lifecycle.csv")

# View summary
print(df.head())
print(df['status'].value_counts())
```

---

## Research Context

This dataset was created to support research work on intelligent certificate lifecycle management and behavioral certificate misuse detection in secure communication networks. It is designed to be lightweight, interpretable, and compatible with common machine learning libraries such as TensorFlow, PyTorch, and Scikit-learn.

---

## License

This dataset is provided for **research and educational purposes only**. You are free to use, modify, and distribute it with appropriate reference to this repository.

---

If you use this dataset in your research, please consider acknowledging this repository.
