# Comparative analysis of major Kubernetes versions

The following types of Kubernetes tools were selected for comparison:

1. **Minikube** is local Kubernetes, focusing on making it easy to learn and develop for Kubernetes.
2. **Kind** is a tool for running local Kubernetes clusters using Docker container “nodes”. 
Kind was primarily designed for testing Kubernetes itself, but may be used for local development or CI.
3. **K3d** is a lightweight wrapper to run k3s (Rancher Lab’s minimal Kubernetes distribution) in docker.
k3d makes it very easy to create single- and multi-node k3s clusters in docker, e.g. for local development on Kubernetes.

## Comparison table of the Kubernetes tool

|   |  minikube[^3][^4]  |  kind[^5]<br>(k8s in Docker)  |  k3d[^6]<br>(k3s in Docker)  |
|---|------------|--------|-------|
| Operating System[^1] | Linux, Windows, MacOS| Linux, Windows, MacOS |  Linux, Windows, MacOS  |
| Supported architectures[^2] | Linux (x86-64 ARM64 ARMv7 ppc64 s390x),<br>macOS (x86-64 ARM64),<br>Windows (x86-64) | Linux (x86-64 ARM64),<br>macOS (x86-64 ARM64),<br>Windows (x86-64) | Linux (x86-64 ARM64),<br>macOS (x86-64 ARM64),<br>Windows (x86-64) |
| Automation | Minikube provides a Command-Line Interface (CLI) that allows automating deployment and cluster management processes.[^7] | Kind provides the capability to automate the creation and management of local Kubernetes clusters through its CLI. | K3d offers a convenient CLI for automating the creation and management of local Kubernetes clusters. |
| Additional Features[^8] | Minikube offers additional features such as the ability to develop and test containers locally. | Kind provides a cluster configuration files and feature gates to enable experimental Kubernetes features and plenty of other configuration options. | K3d provides a cluster configuration file. It allows development teams to persist the configuration of a k3d cluster to a local YAML file that can be shared across the team. |
| Monitoring |	+	 |  -  |	-  |
| Load Balancing  |	External add-ons required |	Built-in |	Built-in |
| Podman	   |  +	 |  +	 |  +  |

## Advantages and Disadvantages

|        | Advantages  |  Disadvantages  |
|--------|-------------|-----------------|
| **Minikube** | Convenient for development and testing on a local computer.</br>Easy to use and configure.</br>Support for a wide range of operating systems and architectures. | Limited scalability options. |
| **Kind**     | Easy to use and configure.</br>Ability to customize different cluster configuration options.</br>Fast cluster deployment.  | Potential resource issues as it uses Docker containers. |
| **K3d**      | Rapid creation and testing of clusters.</br>Ability to monitor and manage Kubernetes clusters.</br>Convenient CLI for automating operations. | Requires the installation of RKE to support more complex scenarios.  |

## Demo

![demo.gif]()

## Summary

Minikube is slightly ahead of all options and the closest to the official Kubernetes development roadmap. Especially, for a single developer the entry barrier seems quite low. Or for the purpose of organizing presentations on one computer or laptop. 
But in my opinion, for a small development team like the "AsciiArtify" startup, should choose between the remaining two options. Thus, taking into account the comparison of working parameters, I would like to recommend using a multiple lightweight Kubernetes cluster like Kind - the best chois for scenarios where you need to create Kubernetes clusters using Docker containers as nodes, with easy setup, team configuration, for testing and development purposes. 

[^1]: [https://shipit.dev/posts/minikube-vs-kind-vs-k3s.html](https://shipit.dev/posts/minikube-vs-kind-vs-k3s.html)
[^2]: [https://microk8s.io/compare](https://microk8s.io/compare)
[^3]: [https://carmencincotti.com/2023-03-06/how-to-use-kubernetes-for-free-on-wsl/](https://carmencincotti.com/2023-03-06/how-to-use-kubernetes-for-free-on-wsl/)
[^4]: [https://minikube.sigs.k8s.io/docs/start/](https://minikube.sigs.k8s.io/docs/start/)
[^5]: [https://kind.sigs.k8s.io/docs/user/quick-start/](https://kind.sigs.k8s.io/docs/user/quick-start/)
[^6]: [https://k3d.io/](https://k3d.io/)
[^7]: [https://ramesh-sahoo.medium.com/kubernetes-dashboard-and-metrics-server-installation-on-docker-desktop-minikube-5c46997120ca](https://ramesh-sahoo.medium.com/kubernetes-dashboard-and-metrics-server-installation-on-docker-desktop-minikube-5c46997120ca)
[^8]: [https://www.blueshoe.io/blog/minikube-vs-k3d-vs-kind-vs-getdeck-beiboot/](https://www.blueshoe.io/blog/minikube-vs-k3d-vs-kind-vs-getdeck-beiboot/)
