

# 🏛️ System Architecture: charlenecordero.com

This document describes the high-level system design and technical invariants of the portfolio platform. It serves as a map for developers to understand the "under the hood" mechanics of the site.

---

## 🗺️ High-Level Component Map
The system follows a **Cloud-Native Layered Architecture**, prioritizing serverless scalability and automated delivery.

| Layer | Responsibility | Technology |
| :--- | :--- | :--- |
| **Compute** | Serverless container orchestration | Google Cloud Run |
| **Logic** | Event handling & SSR rendering | Node.js (Express) |
| **Pipeline** | Automated build & deploy (CI/CD) | Google Cloud Build |
| **Registry** | Container image versioning | Artifact Registry |

---

## 🛠️ Neural Integration (AI Workflow)
This project employs an **Agentic Development** pattern. The architecture was scaffolded and debugged using a collaborative "Agent-Human" loop.

* **Prompt-Driven UI:** Complex CSS modules were designed using specialized AI prompts to ensure mathematical precision.
* **Automated Debugging:** CI/CD errors and IAM permission issues were resolved by utilizing AI agents to analyze cloud logs in real-time.

---

## 📂 Codebase Organization
The repository is organized by functional concern to maintain a clean mental map:

```text
/
├── cloudbuild.yaml      # Entry point for the CI/CD pipeline
├── server.js            # System entry point; handles PORT environments
├── public/              # Atomic UI assets & client-side scripts
│   └── css/             # Responsive grid & flexbox utility systems
├── views/               # SSR templates for high-speed indexing
└── trigger-config.yaml  # IaC for build triggers