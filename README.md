# Helm Multi-Tier Application

## Project Overview

This project demonstrates deployment of a complete multi-tier application using Helm and Kubernetes.

Architecture:

Frontend → Backend → PostgreSQL

---

## Technologies Used

- Kubernetes
- Helm
- Docker
- PostgreSQL
- YAML
- Linux

---

## Features

- Helm subcharts
- PostgreSQL dependency chart
- Frontend deployment
- Backend deployment
- Helm hooks
- initContainers
- Stateful application deployment

---

## Project Structure

```text
webapp-chart/
├── Chart.yaml
├── values.yaml
├── charts/
├── templates/
│   ├── frontend-deployment.yaml
│   ├── frontend-service.yaml
│   ├── backend-deployment.yaml
│   ├── backend-service.yaml
│   └── db-init-job.yaml
```

---

## Installation

```bash
helm dependency update ./webapp-chart

helm install webapp ./webapp-chart \
  --namespace production \
  --create-namespace \
  --wait
```

---

## Verification

```bash
kubectl get pods -n production

kubectl get svc -n production

helm list -n production
```

---

## Concepts Learned

- Helm architecture
- Parent-child charts
- Helm hooks
- Stateful applications
- initContainers
- Multi-tier deployments

---


