---
title: "Best Practice for Developing Platforms on Kubernetes"
collection: publications
type: "Publications"
date: 2023-01-29
permalink: /publications/kubernetes-best-practices
---
# Table of Contents
1. [Overview](#overview)
2. [Summary of Practices](#summary-of-practices)
3. [Other Notable Practices](#other-notable-practices)

## Overview
As businesses strive for digital transformation and the ability to quickly innovate and meet the needs of their users, there is a growing demand for platforms that are scalable, extensible, and secure. To remain competitive, software must be flexible and able to adapt to changing needs. Kubernetes has become a popular choice for building application platforms due to its ability to provide automation, high availability, and portability out of the box, allowing platform teams to build on top of it with confidence.

There are many use cases for Kubernetes, including self-service platforms for internal development teams to deploy applications, multi-tenant application platforms, multi-cloud deployments, data processing and machine learning services. This post will focus on concepts and practices to consider when building an application platform on Kubernetes, rather than specific technologies.

To start, an essential consideration when building an application platform on Kubernetes is determining whether to use hard or soft multi-tenancy. Soft multi-tenancy involves using software-defined isolation for Kubernetes workloads while sharing the underlying infrastructure, which can be useful for providing a self-service platform for development teams to continuously deploy applications to production without the overhead of managing multiple clusters. Hard multi-tenancy, on the other hand, provides the highest level of security by completely isolating tenants from each other at the infrastructure level, which is important for handling sensitive data or meeting compliance requirements. However, hard multi-tenancy can come with additional costs and tooling for operating multiple Kubernetes clusters while not being able to share compute resources.

Security and supply chain management are also important considerations when building an application platform with Kubernetes. Image scanning can detect vulnerabilities in packages that may be included as part of application libraries or base image dependencies. This can help to reduce the risk of malicious attacks from within the application. Other tactics for enhancing security include scanning Dockerfiles for insecure practices, using signed and scanned images, and implementing network policies to control communication between pods.

Another significant consideration is Quality of Service (QoS). Defining QoS classes upfront, especially on shared infrastructure, helps the scheduler determine workload placement and prioritization when resources such as compute or storage are low. Kubernetes has three QoS classes: Guaranteed, Burstable, and Best Effort. These can be useful for different types of workloads, for example, using Guaranteed for production applications and Best Effort for low-priority cron jobs that can tolerate interruption.

In addition to these considerations, it's essential to have a solid understanding of the underlying infrastructure, including storage, and computing, as well as monitoring and logging to ensure the platform is running smoothly and any issues can be quickly identified and addressed.

Kubernetes, as a platform, offers a wide range of controls and features to accommodate various needs. However, it is necessary to note that different organizations and use cases may require different sets of features. Below is a summary of the controls to consider when implementing a platform on Kubernetes.

## Summary of Practices
* [Namespaces](https://kubernetes.io/docs/concepts/overview/working-with-objects/namespaces/) for shared cluster workload isolation
* [Resource Quotas (e.g., limit resources consumed by a given namespace)](https://kubernetes.io/docs/tasks/administer-cluster/manage-resources/quota-memory-cpu-namespace/)
* Defining correct [compute](https://kubernetes.io/docs/concepts/configuration/manage-resources-containers/) & [probe](https://kubernetes.io/docs/tasks/configure-pod-container/configure-liveness-readiness-startup-probes/) requirements to assist in effectively scheduling workloads
* [SecurityContext](https://kubernetes.io/docs/tasks/configure-pod-container/security-context/) tuning, e.g:
	* Stateless container (e.g., read-only filesystem, a large variety of attacks are carried out from downloading remote payloads, or filesystem manipulation, etc.)
	* Prevent the use of privileged containers, root users, etc.
* [AppArmor](https://kubernetes.io/docs/tutorials/security/apparmor/) enforces profile on pods to execute security controls (e.g., prevent file writes)
* [OPA Gatekeeper](https://kubernetes.io/blog/2019/08/06/opa-gatekeeper-policy-and-governance-for-kubernetes/) enforces constraints on deployment template (e.g. prevent the deployment of privileged containers)
* [Container sandboxing](https://kubernetes.io/docs/concepts/containers/runtime-class/) (e.g., [gVisor](https://github.com/google/gvisor), or [Kata Containers](https://katacontainers.io), useful for running untrusted workloads, these practices can help to mitigate container breakouts). Containers share the same kernel as their hosts, kernel bugs can be an attack vector for untrusted workloads.
	* Some noteworthy CVEs related to container breakouts: CVE-2019-5736, CVE-2016-5195, and [others](https://www.container-security.site/attackers/container_breakout_vulnerabilities.html)
* [Dockerfile best practices](https://docs.docker.com/develop/develop-images/dockerfile_best-practices/)
* Scanning images with the admission controller web hook (e.g., scanning images on deployment, and rejecting images with vulnerabilities, etc.)
* Whitelisting permitted images (e.g., to mitigate image squatting attacks, or only permitting trusted repositories, etc.)
* [Cluster audit logging](https://kubernetes.io/docs/tasks/debug/debug-cluster/audit/)
* [Network policies (e.g., Limiting ingress/egress)](https://kubernetes.io/docs/concepts/services-networking/network-policies/). Implementing granular or less permissive network policies. Implementing granular or less permissive network policies can help in mitigating security exploits.
* [Falco](https://falco.org) to monitor containers for malicious activity (e.g., alerting on in-container shell command being executed )

## Other Notable Practices
* CI/CD pipelines for application and cluster deployments
* [Helm templating engine for standardizing platform deployments](https://helm.sh)



