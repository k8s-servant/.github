## k8s-servant

**An open-source, read-only AI SRE agent for Kubernetes.**

k8s-servant looks into your cluster through
[kubernetes-mcp-server](https://github.com/containers/kubernetes-mcp-server) and a
guarded `kubectl`, investigates problems with an LLM, runs scheduled health checks and
posts reports. It can't change cluster state, and it never reads Secrets.

- [k8s-servant/k8s-servant](https://github.com/k8s-servant/k8s-servant): the agent, its container image and Helm chart
- [Contributing](https://github.com/k8s-servant/k8s-servant/blob/main/CONTRIBUTING.md) · [Code of Conduct](https://github.com/k8s-servant/.github/blob/main/CODE_OF_CONDUCT.md) · [Security](https://github.com/k8s-servant/.github/blob/main/SECURITY.md)
