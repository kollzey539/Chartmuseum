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
```

---

## 🚀 CI/CD

This project includes a GitHub Actions workflow that automates packaging and deployment of the Helm chart to a ChartMuseum repository.

### 🔄 Trigger Conditions

The workflow runs automatically when changes are pushed to the `main` branch and affect either of the following paths:

```yaml
- "hash-store/Chart.yaml"
- "hash-store/templates/**"
