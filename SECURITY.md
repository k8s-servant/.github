# Security policy

## Reporting a vulnerability

**Please do not open public issues for security problems.**

Report vulnerabilities privately through GitHub's
[private vulnerability reporting](https://docs.github.com/en/code-security/security-advisories/guidance-on-reporting-and-writing-information-about-vulnerabilities/privately-reporting-a-security-vulnerability):
open the affected repository, go to **Security → Report a vulnerability**, or use
[this link for k8s-servant](https://github.com/k8s-servant/k8s-servant/security/advisories/new).

If you cannot use GitHub's form, email **security@k8s-servant.dev** instead. Please
don't include exploit details in the first message if you'd rather agree on an
encrypted channel first.

Please include:

- affected version (image tag, chart version or commit)
- a description of the issue and its impact
- steps to reproduce or a proof of concept
- any suggested fix

We aim to acknowledge reports within **3 business days** and to agree on a disclosure
timeline with you. We credit reporters in the advisory unless you prefer to stay anonymous.

## Supported versions

Until `v1.0`, only the latest release receives security fixes.

## Scope

k8s-servant is designed to be **read-only**. Anything that lets the agent change
cluster objects, read Secrets, escalate its RBAC, escape the kubectl allow-list, or leak
credentials (LLM keys, webhook URLs, service-account tokens) is a vulnerability,
including through prompt injection from cluster data.

Release images are signed with [cosign](https://github.com/sigstore/cosign) (keyless)
and ship with SBOM and provenance attestations.
