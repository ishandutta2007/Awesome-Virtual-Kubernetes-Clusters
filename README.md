# Awesome-Virtual-Kubernetes-Clusters

# Top Virtual Kubernetes Clusters Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Virtual Clusters, Multi-Tenancy, Namespace Isolation, Nested Control Planes & Kubernetes-as-a-Service Patterns*  
**Last updated: October 2026**

This repository tracks notable **SaaS/hosted platforms** and **open-source projects** for **Virtual Kubernetes Clusters**. These systems give teams a full (or nearly full) cluster API—often with a dedicated control plane—while sharing underlying worker capacity for density, cost control, and safer multi-tenancy.

**Examples** include managed Kubernetes (EKS/AKS/GKE), Red Hat OpenShift, Rancher, VMware Tanzu, Mirantis, Platform9, Nutanix Karbon, SUSE offerings, and **vCluster** (`loft-sh/vcluster`)—create fully functional virtual Kubernetes clusters effortlessly.

**Open-source emphasis**: Virtual cluster technology is led by open source. **vCluster**, **Kamaji**, **Cluster API**, and related multi-tenancy projects enable nested and lightweight control planes. This section is heavily expanded.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Amazon EKS, Azure AKS, Google GKE](https://aws.amazon.com/eks/)**  
  Managed Kubernetes control planes—each tenant or team typically gets an isolated cluster rather than a virtual cluster on shared hosts.

- **[Red Hat OpenShift, Rancher Prime, VMware Tanzu, Mirantis, Platform9, Nutanix](https://www.redhat.com/en/technologies/cloud-computing/openshift)**  
  Enterprise Kubernetes platforms with multi-cluster management, policy, and tenant isolation features (projects, namespaces, or dedicated clusters).

- **[Loft / vCluster Platform (commercial)](https://www.vcluster.com/)**  
  Commercial management plane around vCluster—virtual clusters as a product for platform teams.

- **[Other managed Kubernetes & multi-tenant platforms](https://cloud.google.com/kubernetes-engine)**  
  Additional hosted K8s and fleet-management services.

## Open-Source GitHub Projects

### Virtual Cluster Engines

- **[vCluster](https://github.com/loft-sh/vcluster)**  
  Leading open-source virtual Kubernetes clusters—run full control planes inside namespaces on a host cluster; high density and strong isolation for tenants and ephemeral environments.

- **[Kamaji](https://github.com/clastix/kamaji)**  
  Open-source Kubernetes control plane manager—hosted control planes as multi-tenant “Cluster as a Service” on a management cluster.

- **[Cluster API](https://github.com/kubernetes-sigs/cluster-api)**  
  Open declarative API for creating, updating, and managing Kubernetes clusters—foundation for many virtual and managed cluster workflows.

- **[k3k / lightweight nested experiments](https://github.com/search?q=virtual+kubernetes+cluster)**  
  Community projects exploring nested or minimal virtual clusters for edge and lab use.

### Multi-Tenancy & Isolation Building Blocks

- **[Hierarchical Namespace Controller (HNC)](https://github.com/kubernetes-sigs/hierarchical-namespaces)**  
  Open multi-tenancy helper—namespace hierarchies and policy inheritance on a shared cluster.

- **[Capsule](https://github.com/projectcapsule/capsule)**  
  Open multi-tenant operator—tenants, quota, and policy boundaries on shared Kubernetes.

- **[Kyverno / OPA Gatekeeper](https://github.com/kyverno/kyverno)**  
  Open policy engines used to enforce isolation and guardrails for virtual or shared clusters.

- **[Liqo](https://github.com/liqotech/liqo)**  
  Open multi-cluster resource sharing—offload workloads across clusters in a seamless way.

- **[kcp](https://github.com/kcp-dev/kcp)**  
  Open horizontally scalable control plane for Kubernetes-like APIs—workspace-oriented multi-tenancy research and production paths.

### Lightweight & Nested Platforms

- **[k3s / k0s as inner clusters](https://github.com/k3s-io/k3s)**  
  Lightweight distributions frequently used as the control plane binary inside virtual cluster solutions.

- **[kind / minikube / k3d](https://github.com/kubernetes-sigs/kind)**  
  Open local cluster tools—useful for nested testing and CI, not full multi-tenant production virtualization.

### Additional Strong Open-Source Options

- **Production virtual clusters**: vCluster.
- **Hosted control planes (multi-tenant CaaS)**: Kamaji.
- **Fleet provisioning**: Cluster API.
- **Shared-cluster tenancy**: Capsule + HNC + policy (Kyverno/OPA).
- **Composable stacks**: Host cluster (any conformant K8s) → vCluster/Kamaji → GitOps per virtual cluster.
- Managed K8s still leads when you want a fully isolated, provider-operated control plane per team without operating a host cluster.

**Frameworks for building custom systems**:  
**vCluster** for dense virtual clusters on existing K8s; **Kamaji** for multi-tenant control-plane as a service; **Cluster API** for declarative real clusters; **Capsule/HNC** when namespace-level multi-tenancy is enough.  
Fully open virtual Kubernetes clusters are production-ready for platform engineering and cost-efficient multi-tenancy.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS/hosted or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Virtual clusters share underlying nodes—noisy neighbors, escape risks, and storage classes need careful design. Apply network policies, resource quotas, and hardened host clusters. Ephemeral virtual clusters still require secret and image hygiene.
- Open-source virtual cluster tools offer density and control. Managed Kubernetes shifts control-plane operations to the cloud vendor. Neither replaces workload security and least-privilege RBAC.

---

**Made for platform engineers building multi-tenant Kubernetes and internal developer platforms.**  
Let's expand open virtual clusters while recognizing the operational simplicity of fully managed Kubernetes services.
