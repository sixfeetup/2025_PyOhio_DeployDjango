---
title-prefix: Six Feet Up
pagetitle: "Deploy Django: GitOps & Kubernetes Made Easy"
author: Calvin Hendryx-Parker, CTO, Six Feet Up
author-meta:
    - Calvin Hendryx-Parker
date: PyOhio 2025
date-meta: 2025
keywords:
    - Kubernetes
    -  CI/CD
    -  Django
---

# Deploy Django: GitOps & Kubernetes Made Easy {.semi-filtered data-background-image="images/Chris Linnett Unsplash.jpg"}
#### Calvin Hendryx-Parker, CTO
#### Six Feet Up
### PyOhio 2025

::: notes
We struggled so you don't have to
:::

# Talk Slides
<https://github.com/sixfeetup/2025_PyOhio_DeployDjango>
![](images/presentation_qr.png)

# GitOps: The Operating Model {data-background-image="images/Chuttersnap Unsplash.jpg"}

* **Single Source of Truth**
* **Declarative**
* **Automated Reconciliation**
* **Pull-based Deployments**
* Bonus: **Documentation of Infrastructure and Application**

::: notes
Talk about the old days, which may be the current days for meany folks
* **Single Source of Truth**: Git repository contains all deployment configs
* **Declarative**: Describe *what* you want, not *how* to get there
* **Automated Reconciliation**: System continuously ensures actual state matches desired state
* **Pull-based Deployments**: No more `kubectl apply` from laptops
* **Documentation of Infra**: documentation as code of infra and application
:::

# Why GitOps for Django? {.semi-filtered data-background-image="images/Erwan Hesry Unsplash.jpg"}

* **Rollback = Git Revert**: Instant, auditable rollbacks
* **Environment Drift Prevention**: Dev/Staging/Prod stay in sync
* **Security**: No CI/CD needs cluster credentials
* **Compliance**: Complete audit trail of who changed what, when

::: notes
You control who has access to the KUBECONFIG
:::

# Why Kubernetes for Django? {.semi-filtered data-background-image="images/Frank McKenna Unsplash.jpg"}

* **Resource Efficiency**: Auto-scaling based on actual load
* **Zero-downtime Deployments**: Rolling updates by default
* **Self-healing**: Automatic container restarts
* **Service Discovery**: No more hardcoded URLs
* **Secrets Management**: Built-in, encrypted at rest
* **Control Plane**: Automate releases and orchestration
* **Deploy Story**: Matches Developer Environment
* **Cloud Agnostic**: No vendor lock-in

# Enter Argo CD {.semi-filtered data-background-image="images/Jeffrey Blum Unsplash.jpg"}

<img src="images/argocd.png" style="float: right;width: 200px">

<div style="width: 80%">
* Kubernetes-native continuous delivery
* Watches Git repos for changes
* Syncs automatically or on-demand
* Beautiful UI for visibility
* Supports Helm, Kustomize, plain YAML
</div>

::: notes
Powerful wrapper around kubectl and git
:::
 
# Enabled by Scaf {.semi-filtered data-background-image="images/Kurt Cotoaga Unsplash.jpg"}

<img src="images/scaf_logo.webp" style="float: right;width: 200px">

<div style="width: 80%">
* **Day Zero GitOps**: No retrofitting required
* **Battle-tested**: Years of production experience baked in
* **Cognitive Load Reduction**: Focus on your app, not infrastructure
* **Immutable Infrastructure**: Talos Linux for secure, minimal K8s nodes
</div>

::: notes
The Magic: Best Practices by Default
Scaf solves the "blank page" problem
you don't have to figure out how to structure your k8s configs, how to handle secrets, or how to set up ArgoCD.
It's all there from the start.
:::

# GitOps Flow

![](images/Scaf%20Gitops%20Diagram.png){.r-stretch .r-hstack}

# Nix Solves the Cross-Platform Issues {.r-fit-text .semi-filtered data-background-image="images/Nathan Cima from Unsplash.jpg"}

This could be a talk on its own...

* Apple's BSD `sed` vs Gnu `sed`
* Apple's BSD `base64` vs Gnu `base64`
* Apple's BSD `tr` vs Gnu `tr`

&nbsp;

## Superpowers
* Install common tools
* Make sure the tools versions match

::: notes
sed has some creature comforts on gnu that aren't there on mac
base64 on mac wraps by default, gnu has a command line flag for it
truncate has some creature comforts on gnu that aren't there on mac

Helping another developer shouldn't be a hard experience
No one likes sitting down to a dvorak keyboard when they type on qwerty all day
But each person can still have their own tools and preferences that extend the base
:::

# Hot Off the Presses {.semi-filtered data-background-image="images/Chris Linnett Unsplash.jpg"}

* Decoupled from 1Password
* "Dangerous Mode"
* Sealed Secrets Automated
* Teardown works cleanly
* Github Automation for Variables and Keys
* Updated ArgoCD to latest

::: notes
Now includes more tools managed by Nix such as `gh` and `copier`
:::

# Life Before GitOps vs After {.r-fit-text data-background-image="images/Mika Baumeister Unsplash.jpg"}

:::: {.columns}
::: {.column width="50%"}
### Traditional Deployment 😰
* SSH into servers
* Manual `docker-compose up`
* "Works on my machine"
* Deployment = Anxiety
* Who deployed what?
* How do we rollback?
:::

::: {.column width="50%"}
### GitOps Deployment 🚀
* Git push = Deploy
* Automated & consistent
* Works everywhere
* Deployment = Confidence
* Full audit trail
* Rollback = Git revert
:::
::::

# Start Your GitOps Journey Today {data-background-image="images/Nathan Cima from Unsplash.jpg"}

### 15-Minute Quick Wins:
1. **Install Scaf**: One line installer
2. **Create a Project**: `scaf myproject`
3. **Deploy to AWS**: Login via CLI and deploy
4. **Make a Change**: Edit YAML, commit, watch magic
<hr/>

### You Don't Need:
* Perfect Kubernetes knowledge
* Complex CI/CD pipelines  
* A huge team

::: notes
Lower the barrier to entry - they can start small
:::

# Resources {.semi-filtered data-background-image="images/Erwan Hesry Unsplash.jpg"}

* [Scaf Project Info](https://sixfeetup.com/scaf)
* [Scaf Github Repo](github.com/sixfeetup/scaf)
* [Scaf Full Stack Template](https://github.com/sixfeetup/scaf-fullstack-template)
* [Talk Python to Me Episode on Scaf](https://talkpython.fm/episodes/show/496/scaf-complete-blueprint-for-new-python-kubernetes-projects)

# Talk To Me{.r-fit-text}

📩 <calvin@sixfeetup.com>  
🤝 <https://linkedin.com/in/calvinhp>  
✖️ [@calvinhp](https://x.com/calvinhp)  
🐘 [@calvinhp@fosstodon.org](https://fosstodon.org/@calvinhp)  
🦋 [@calvinhp.com](https://bsky.app/profile/calvinhp.com)
