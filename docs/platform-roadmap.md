# Alpha Engine Platform Roadmap

## Completed

- Kubernetes cluster
- Helm-based deployment
- PostgreSQL
- Prometheus
- Grafana
- PostgreSQL Exporter
- GitHub Actions
- GHCR
- ArgoCD
- GitOps deploy for Alpha Engine
- Loki
- Promtail
- Grafana dashboard provisioning
- Runtime metrics and logs

## Current Focus: Observability GitOps

### 7.1 Move Observability to ArgoCD

- Create ArgoCD Application for monitoring
- Create ArgoCD Application for loki
- Create ArgoCD Application for promtail
- Verify self-healing by deleting provisioned resources

### 7.2 Alertmanager

- Understand Prometheus alert rules
- Configure first alert
- Add Grafana/Prometheus alert visibility
- Later: Telegram notifications

## Stage 8: Security

### 8.1 TLS and cert-manager

- Install cert-manager
- Understand Issuer and ClusterIssuer
- Add TLS to Ingress
- Prepare for real DNS / Let's Encrypt

### 8.2 Secrets Management

- Study Kubernetes Secrets limitations
- Install and test HashiCorp Vault
- Compare with External Secrets Operator, SOPS, Sealed Secrets
- Move sensitive values out of plain manifests

### 8.3 RBAC

- Understand ServiceAccount, Role, ClusterRole, RoleBinding
- Review permissions of platform components
- Apply least privilege where practical

### 8.4 NetworkPolicy

- Understand default allow vs default deny
- Restrict Alpha Engine to PostgreSQL and required services
- Restrict PostgreSQL access
- Test allowed and blocked traffic

### 8.5 Container Security

- Run containers as non-root where possible
- Drop Linux capabilities
- Use readOnlyRootFilesystem where possible
- Configure seccomp
- Add resource limits and requests review

## Future Stages

### Stage 9: Real CI

- Ruff
- Black
- MyPy
- Pytest
- Trivy image scanning

### Stage 10: Advanced GitOps

- ArgoCD Image Updater
- Compare current infra-repo commit approach
- Sync waves and app-of-apps

### Stage 11: High Availability

- PostgreSQL backups
- Velero
- Storage strategy
- Disaster recovery testing

### Stage 12: Kubernetes Advanced

- HPA
- PDB
- Affinity / Anti-affinity
- Topology spread constraints

### Stage 13: Kubernetes Security

- OPA Gatekeeper or Kyverno
- Policy-as-code
- Image policy
- Admission control

### Stage 14: GitLab Migration

- Compare GitHub Actions and GitLab CI
- Move CI pipeline
- Keep ArgoCD/GitOps architecture

### Stage 15: Production Cluster

- Production-ready Kubernetes distribution
- Real DNS
- TLS
- Backups
- Monitoring
- Security baseline
