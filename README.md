# ☸️ Cloud-Native Personal Bio & Portfolio

This repository hosts my personal bio website and project portfolio. More importantly, it serves as a live demonstration of my **DevOps, GitOps, and Kubernetes** engineering workflows. 

Instead of deploying to a standard static host, this portfolio is fully containerized, managed via Infrastructure as Code (IaC), and orchestrated inside a Kubernetes cluster.

---

## 🛠️ Tech Stack & Architecture

* **Frontend:** Astro / TailwindCSS (Lightweight, performance-optimized static site)
* **Containerization:** Docker (Multi-stage builds for minimal image size)
* **CI/CD:** GitHub Actions (Automated linting, testing, and Docker builds)
* **Registry:** GitHub Container Registry (GHCR)
* **Orchestration:** Kubernetes (K3s home-lab / Cloud managed cluster)
* **GitOps:** ArgoCD (Automated synchronization from this repo to the cluster)

---

## 📁 Repository Structure

```text
├── .github/workflows/      # CI/CD Pipelines (Build & Push)
├── site/                   # Frontend website code (Bio & Portfolio pages)
│   ├── content/            # Markdown files for easy content updates
│   └── Dockerfile          # Multi-stage production Docker build
├── k8s/                    # Cloud-native infrastructure manifests
│   ├── deployment.yaml     # Application deployment with health checks
│   ├── service.yaml        # Internal cluster networking
│   └── ingress.yaml        # External traffic routing & TLS
└── README.md               # You are here!