<div align="center">

# homelab

<!-- ANCHOR: introduction -->

[![stars](https://img.shields.io/github/stars/tuthvn/homelab?logo=github&logoColor=white&color=gold&style=flat-square)](https://github.com/tuthvn/homelab)

This project utilizes [Infrastructure as Code](https://en.wikipedia.org/wiki/Infrastructure_as_code) and [GitOps](https://www.weave.works/technologies/gitops) to automate provisioning, operating, and updating self-hosted services in my homelab.
It can be used as a highly customizable framework to build your own homelab.

<!-- TODO -->

<!-- ANCHOR_END: introduction -->

Current status: **ALPHA**

</div>

## Overview

This section provides a high level overview of the project.

### Hardware

![Hardware]()


### Features

Project status: **Alpha** (see [roadmap](#roadmap) below)

- [ ] Common applications: Gitea, Seafile, Jellyfin, Paperless...
- [ ] Automated bare metal provisioning with PXE boot
- [ ] Automated Kubernetes installation and management
- [ ] Installing and managing applications using GitOps
- [ ] Modular architecture, easy to add or remove features/components
- [ ] Automated certificate management
- [ ] Automatically update DNS records for exposed services
- [ ] Expose services to the internet securely with [Cloudflare Tunnel](https://www.cloudflare.com/products/tunnel/)
- [ ] CI/CD platform
- [ ] Private container registry
- [ ] Distributed storage
- [ ] Support multiple environments (dev, prod)
- [ ] Monitoring and alerting
- [ ] Automated offsite backups
- [ ] Single sign-on


### Tech stack

<table>
  <tr>
    <th>Logo</th>
    <th>Name</th>
    <th>Description</th>
  </tr>
  <tr>
    <td><img width="32" src="https://simpleicons.org/icons/ansible.svg"></td>
    <td><a href="https://www.ansible.com">Ansible</a></td>
    <td>Automate bare metal provisioning and configuration</td>
  </tr>
  <tr>
    <td><img width="32" src="https://cncf-branding.netlify.app/img/projects/argo/icon/color/argo-icon-color.svg"></td>
    <td><a href="https://argoproj.github.io/cd">ArgoCD</a></td>
    <td>GitOps tool built to deploy applications to Kubernetes</td>
  </tr>
  <tr>
    <td><img width="32" src="https://github.com/jetstack/cert-manager/raw/master/logo/logo.png"></td>
    <td><a href="https://cert-manager.io">cert-manager</a></td>
    <td>Cloud native certificate management</td>
  </tr>
  <tr>
    <td><img width="32" src="https://avatars.githubusercontent.com/u/314135?s=200&v=4"></td>
    <td><a href="https://www.cloudflare.com">Cloudflare</a></td>
    <td>DNS and Tunnel</td>
  </tr>
  <tr>
    <td><img width="32" src="https://www.docker.com/sites/default/files/d8/2019-07/Moby-logo.png"></td>
    <td><a href="https://www.docker.com">Docker</a></td>
    <td>Ephermeral PXE server and convenient tools container</td>
  </tr>
  <tr>
    <td><img width="32" src="https://upload.wikimedia.org/wikipedia/commons/b/bb/Gitea_Logo.svg"></td>
    <td><a href="https://gitea.com">Gitea</a></td>
    <td>Self-hosted Git service</td>
  </tr>
  <tr>
    <td><img width="32" src="https://grafana.com/static/img/menu/grafana2.svg"></td>
    <td><a href="https://grafana.com">Grafana</a></td>
    <td>Operational dashboards</td>
  </tr>
  <tr>
    <td><img width="32" src="https://cncf-branding.netlify.app/img/projects/helm/icon/color/helm-icon-color.svg"></td>
    <td><a href="https://helm.sh">Helm</a></td>
    <td>The package manager for Kubernetes</td>
  </tr>
  <tr>
    <td><img width="32" src="https://cncf-branding.netlify.app/img/projects/k3s/icon/color/k3s-icon-color.svg"></td>
    <td><a href="https://k3s.io">K3s</a></td>
    <td>Lightweight distribution of Kubernetes</td>
  </tr>
  <tr>
    <td><img width="32" src="https://cncf-branding.netlify.app/img/projects/kubernetes/icon/color/kubernetes-icon-color.svg"></td>
    <td><a href="https://kubernetes.io">Kubernetes</a></td>
    <td>Container-orchestration system, the backbone of this project</td>
  </tr>
  <tr>
    <td><img width="32" src="https://github.com/grafana/loki/blob/main/docs/sources/logo.png?raw=true"></td>
    <td><a href="https://grafana.com/oss/loki">Loki</a></td>
    <td>Log aggregation system</td>
  </tr>
  <tr>
    <td><img width="32" src="https://cncf-branding.netlify.app/img/projects/longhorn/icon/color/longhorn-icon-color.svg"></td>
    <td><a href="https://longhorn.io">Longhorn</a></td>
    <td>Cloud native distributed block storage for Kubernetes</td>
  </tr>
  <tr>
    <td><img width="32" src="https://avatars.githubusercontent.com/u/60239468?s=200&v=4"></td>
    <td><a href="https://metallb.org">MetalLB</a></td>
    <td>Bare metal load-balancer for Kubernetes</td>
  </tr>
  <tr>
    <td><img width="32" src="https://avatars.githubusercontent.com/u/1412239?s=200&v=4"></td>
    <td><a href="https://www.nginx.com">NGINX</a></td>
    <td>Kubernetes Ingress Controller</td>
  </tr>
  <tr>
    <td><img width="32" src="https://cncf-branding.netlify.app/img/projects/prometheus/icon/color/prometheus-icon-color.svg"></td>
    <td><a href="https://prometheus.io">Prometheus</a></td>
    <td>Systems monitoring and alerting toolkit</td>
  </tr>
  <tr>
    <td><img width="32" src="https://avatars.githubusercontent.com/u/75713131?s=200&v=4"></td>
    <td><a href="https://rockylinux.org">Rocky Linux</a></td>
    <td>Base OS for Kubernetes nodes</td>
  </tr>
  <tr>
    <td><img width="32" src="https://avatars.githubusercontent.com/u/47602533?s=200&v=4"></td>
    <td><a href="https://tekton.dev">Tekton</a></td>
    <td>Cloud native solution for building CI/CD systems</td>
  </tr>
  <tr>
    <td><img width="32" src="https://trow.io/trow.png"></td>
    <td><a href="https://trow.io">Trow</a></td>
    <td>Private container registry</td>
  </tr>
  <tr>
    <td><img width="32" src="https://simpleicons.org/icons/vault.svg"></td>
    <td><a href="https://www.vaultproject.io">Vault</a></td>
    <td>Secrets and encryption management system</td>
  </tr>
</table>

## Get Started


## Roadmap


## Contributing

Any contributions you make, either big or small, are greatly appreciated.

## License



## Acknowledgements

- [ArgoCD usage in my coworker's homelab](https://github.com/locmai/humble)
- [README template](https://github.com/othneildrew/Best-README-Template)
- [Run the same Cloudflare Tunnel across many `cloudflared` processes](https://developers.cloudflare.com/cloudflare-one/tutorials/many-cfd-one-tunnel)
- [MAC address environment variable in GRUB config](https://askubuntu.com/questions/1272400/how-do-i-automate-network-installation-of-many-ubuntu-18-04-systems-with-efi-and)
- [Official k3s systemd service file](https://github.com/k3s-io/k3s/blob/master/k3s.service)
- [Official Cloudflare Tunnel examples](https://github.com/cloudflare/argo-tunnel-examples)
- [Initialize GitOps repository on Gitea and integrate with Tekton by RedHat](https://github.com/redhat-scholars/tekton-tutorial/tree/master/triggers)

## Stargazers over time

