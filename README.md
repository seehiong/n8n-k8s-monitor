# n8n-k8s-monitor

Helper workflows and scripts used to monitor and troubleshoot Kubernetes clusters using n8n.

This repository accompanies the article **"Self-Healing Kubernetes with n8n"**, where n8n is deployed inside a Kubernetes cluster and used to perform automated health checks, root cause analysis, and remediation workflows.

The workflows in this repository demonstrate how n8n can execute operational commands such as `kubectl` and `talosctl` to inspect cluster state and automate diagnostics.

## Purpose

This repository provides supporting assets for:

- Kubernetes cluster health monitoring
- Automated diagnostics using `kubectl`
- Talos node inspection using `talosctl`
- AI-assisted root cause analysis workflows
- Human-in-the-loop remediation approval

## Components

Typical checks performed by these workflows include:

- Non-running pods
- CrashLoopBackOff pods
- Pending pods
- Node readiness
- Failed jobs
- Storage issues
- Cluster-wide events

The results are aggregated and passed to downstream workflows for analysis and notification.

## Requirements

- Kubernetes cluster access
- `kubectl` available inside the execution environment
- `talosctl` (optional, for Talos clusters)
- n8n instance capable of running shell commands

## Usage

Import the workflow JSON files into your n8n instance and adjust any cluster-specific commands or namespaces.

These workflows are designed to be triggered periodically using an n8n **Schedule Trigger**.

## Related Project

The full architecture and deployment setup are described in the accompanying article:

**Self-Healing Kubernetes with n8n**

## License

MIT
