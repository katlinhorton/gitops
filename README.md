<h1 align="center">
  It's My k8s in a Box
  <br />
  <br />
  <img src="https://i.imgur.com/p1RzXjQ.png">
</h1>
<br />
<div align="center">

[![Discord](https://img.shields.io/badge/discord-chat-7289DA.svg?maxAge=60&style=flat-square)](https://discord.gg/DNCynrJ)

</div>

---

# :book:&nbsp; Overview

Welcome to my home Kubernetes cluster. This repo _is_ my Kubernetes cluster in a declarative state. [Flux](https://github.com/fluxcd/flux) and [Helm Operator](https://github.com/fluxcd/helm-operator) watch my [cluster](./cluster/) folder and makes the changes to my cluster based on the yaml manifests.

Feel free to join our [Discord](https://discord.gg/DNCynrJ) if you have any questions.

---

## :computer:&nbsp; Hardware configuration

_All my Kubernetes master and worker nodes below are running bare metal Ubuntu 20.04.x_

| Device                  | Count | OS Disk Size            | Data Disk Size                           | Ram  | Purpose |
|-------------------------|-------|-------------------------|------------------------------------------|------|---------|
| Raspberry Pi 4          | 3     | 120GB (USB Booting SSD) | N/A                                      | 4 GB | k8s Masters |
| Dell R610               | 3     | 2x 120GB SSD (RAID1)    | 2x 1TB HDD (RAID0, longhorn)             | 48GB | k8s Workers |
| Xyratex HB-1235         | 1     | N/A                     | 3x 4TB HDD (nfs)                         | N/A  | ZFS Main Storage |

---

## :memo:&nbsp; IP addresses

_This table is a reference to IP addresses in my deployments and may not be fully up-to-date_

| Deployment               | Address        |
|--------------------------|----------------|
| nginx-ingress (external) | 192.168.130.100 |
| longhorn                 | 192.168.130.104 |

---

## :handshake:&nbsp; Thanks

A lot of inspiration for this repo came from the following people:

- [billimek/k8s-gitops](https://github.com/billimek/k8s-gitops)
- [carpenike/k8s-gitops](https://github.com/carpenike/k8s-gitops)
- [dcplaya/k8s-gitops](https://github.com/dcplaya/k8s-gitops)
- [rust84/k8s-gitops](https://github.com/rust84/k8s-gitops)
- [blackjid/homelab-gitops](https://github.com/blackjid/homelab-gitops)
- [bjw-s/k8s-gitops](https://github.com/bjw-s/k8s-gitops)
- [nlopez/k8s_home](https://github.com/nlopez/k8s_home)
- [onedr0p/k3s-gitops](https://github.com/onedr0p/k3s-gitops)
