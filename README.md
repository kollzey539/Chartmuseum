# Hash Store Helm Chart

A Helm chart for deploying the **Hash Store API** — a simple web service that stores and retrieves string values based on their SHA-256 hash.  
This chart packages all necessary Kubernetes components, including deployment, service, ingress, and configuration.

---

## 📁 Project Structure

```text
.
├── hash-store/
│   ├── Chart.yaml          # Chart metadata
│   ├── values.yaml         # Default configuration values
│   ├── templates/          # Kubernetes manifests
│   │   ├── _helpers.tpl    # Template helper definitions
│   │   ├── deployment.yaml # Deployment manifest
│   │   ├── ingress.yaml    # Ingress manifest
│   │   ├── service.yaml    # Service manifest
├── .github/
│   └── workflows/
│       └── Helm-package.yaml # CI pipeline to package and push Helm chart
├── README.md

