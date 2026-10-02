# Sandaru Wijewardhana

**Kubernetes · Go · software engineering**

I am passionate about contributing to Kubernetes and the other infrastructure I run every day, especially the kind of bug CI cannot catch on its own goroutines that can never be woken controllers that never converge.

I build and run **BayWork** ([baywork.lk](https://baywork.lk)), a multi-tenant ERP SaaS for vehicle service stations written and operated alone, in production with paying customers. During my WSO2 internship I built a Kubernetes registry operator in Go that provisions a private Harbor registry per namespace.

Software engineering intern at [WSO2](https://wso2.com). BSc Eng (Hons) in Computer Engineering, University of Peradeniya.

### Merged upstream

- **[kubernetes/kubernetes #141955](https://github.com/kubernetes/kubernetes/pull/141955)** — fixed two leaked goroutines in kube-controller-manager caused by passing a nil stop channel to secure serving, making the graceful-shutdown path reachable again.
- **[prometheus/prometheus #19522](https://github.com/prometheus/prometheus/pull/19522)** — fixed an empty remote-write panel for native histogram scrapes by adding `histogram_quantile` queries beside the classic `_bucket` ones.
- **[keycloak/keycloak #51935](https://github.com/keycloak/keycloak/pull/51935)** — fixed SCIM filtered PATCH removal deleting entire multivalued attributes, and made unsupported filters return HTTP 400 instead of 500.
- **[argoproj/argo-cd #29255](https://github.com/argoproj/argo-cd/pull/29255)** — hid the pod-highlight button for single-pod resources and cleared stale highlights when log queries change.
- **[kubernetes-sigs/kubespray #13437](https://github.com/kubernetes-sigs/kubespray/pull/13437)** — upgraded nerdctl to v2.3.5 and unblocked automated version tracking that an ARM checksum gap had capped at 2.2.x.
- **[cncf/k8s-conformance #4395](https://github.com/cncf/k8s-conformance/pull/4395)** — CNCF Certified Kubernetes conformance results for Kubespray v2.31.0 on Kubernetes v1.35.4: 441 specs, 0 failures.
- **[ceph/ceph-csi #6508](https://github.com/ceph/ceph-csi/pull/6508)** — moved subvolume pinning onto go-ceph's typed API, enabling non-default subvolume groups.

### Open

- **[kubernetes/kubernetes #141850](https://github.com/kubernetes/kubernetes/pull/141850)** — end-to-end goroutine leak check on Go 1.27's leak profile, across the API server, kubelets, controller-manager and scheduler. It found the leaks fixed in #141955.
- **[kubernetes/kubernetes #142189](https://github.com/kubernetes/kubernetes/pull/142189)** — stops the Deployment controller creating ReplicaSets indefinitely when a feature gate is disabled while a pod template field is still in use.
- **[helm/helm #32568](https://github.com/helm/helm/pull/32568)** — fixed provenance key loss in concatenated keyrings caused by `armor.Decode` reading past a block boundary.
- **[thunder-id/thunderid #5206](https://github.com/thunder-id/thunderid/pull/5206)** — separated unknown from empty attribute profiles in consent filtering to stop redundant prompts.

### Projects

- **BayWork** — multi-tenant workshop-management SaaS, built and operated alone, in production with paying customers. Schema-per-tenant PostgreSQL, offline-tolerant mutation queue with idempotency keys, p95 under 120 ms. [baywork.lk](https://baywork.lk)
- **[Registry-as-a-Service](https://github.com/sandaruwijewardhana/harbor-operator)** — Go operator provisioning per-namespace Harbor registries on RKE2/Harvester. A 7-pod tenant registry in under 2.5 minutes instead of about an hour by hand, with 3-tier storage autoscaling cutting per-tenant storage ~80%.
- **Harvester upgrade acceptance suite** — Go and Ginkgo acceptance tests that prove platform capabilities still work after a Harvester or Rancher upgrade, replacing a day of manual post-upgrade checks.

### Research & publications

**[Explainable-AI zero-trust anomaly detection for encrypted traffic](https://cepdnaclk.github.io/e20-4yp-Explainable-AI-Driven-Zero-Trust-Anomaly-Detection-for-Encrypted-Traffic/)** — accepted for publication at iPURSE 2026. Lead architect. Detecting attacks in encrypted traffic without decrypting it, with every decision explained. A 1.2 ms Decision Tree triage stage ahead of deep analysis gave a 2.6× speed-up while holding 96.69% accuracy and 99.31% attack recall.

[Portfolio](https://sandaruwijewardhana.github.io/portfolio/) · [LinkedIn](www.linkedin.com/in/sandaru-wijewardhana-8b7009244) · sandaruwijewardhana@gmail.com
