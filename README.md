<p align="center">
  Christian Lehnert &nbsp;·&nbsp; Infra · Automation · DevOps &nbsp;·&nbsp; Self-hosting since 2012 &nbsp;·&nbsp; 🇨🇭
</p>

<p align="center">
  <img src="https://img.shields.io/github/last-commit/christianlehnert/christianlehnert?style=flat-square&label=last%20commit&color=3EF71A" />
  <img src="https://img.shields.io/github/followers/christianlehnert?style=flat-square&label=followers&color=3EF71A" />
  <img src="https://komarev.com/ghpvc/?username=christianlehnert&style=flat-square&color=3EF71A&label=profile+views" />
</p>

> Ops side of things. For backend, security and the rest, see my main account → **[@chfle](https://github.com/chfle)**

## whoami

```bash
$ cat /etc/motd
  role     : infra / automation / devops
  os       : Debian, everywhere
  rule #1  : if you do it twice, script it
  rule #2  : if it's not in git, it doesn't exist
  rule #3  : own the hardware, own the keys
```

Everything under `c0xl.ch` runs on my own metal: racked, networked, provisioned
and monitored by me. This account is where the plumbing lives — configs,
playbooks, pipelines, scripts.

## Infra — live

![c0xl.ch](https://status.c0xl.ch/api/badge/1/status?style=flat-square&label=c0xl.ch)
![chat.c0xl.ch](https://status.c0xl.ch/api/badge/2/status?style=flat-square&label=xmpp)
![sync.c0xl.ch](https://status.c0xl.ch/api/badge/3/status?style=flat-square&label=vpn)
![pdf.c0xl.ch](https://status.c0xl.ch/api/badge/4/status?style=flat-square&label=pdf-mcp)

```
              internet
                 │
        ┌────────┴────────┐
        │  edge / ZBFW    │  Cisco Catalyst · MikroTik RouterOS
        └────────┬────────┘
                 │  VLAN-segmented
     ┌───────────┼─────────────┐
     │           │             │
  WireGuard    Caddy       wstunnel
  (sync.)    (reverse proxy, TLS)
                 │
     ┌───────────┴───────────────────┐
     │  Proxmox cluster — Dell VRTX  │
     │  3× M630 blades               │
     │  VMs + LXC + Docker           │
     └───────────────────────────────┘
```

## Stack — the ops version

| Domain | Tools |
|---|---|
| **Virtualization** | Proxmox VE · KVM · LXC |
| **Containers** | Docker · Docker Compose |
| **Automation** | Bash · Python · Ansible · cron / systemd timers |
| **CI/CD** | GitHub Actions · Git-driven deploys |
| **Networking** | Cisco Catalyst · MikroTik RouterOS · VLAN / ZBFW design · WireGuard · `wstunnel` |
| **Edge** | Caddy · automatic TLS · reverse proxy |
| **Data** | PostgreSQL · MariaDB · Redis — backed up, tested restores |
| **Observability** | Uptime Kuma · logs · alerting |
| **OS** | Debian · i3 · tmux · Vim |

## Principles

- **Infrastructure as code** — no snowflake servers, rebuild from repo
- **Least privilege** — segmented networks, minimal exposed surface, keys not passwords
- **Boring is good** — Debian stable, well-understood tools, fewer moving parts
- **Backups don't exist until restored** — so restores get tested

## Contact

- [christian.lehnert@tutanota.com](mailto:christian.lehnert@tutanota.com)
- PGP fingerprint: `3618 EC2F 46B6 513F 8FC6  0444 7954 E03B 2988 C19B`
- Main account: [@chfle](https://github.com/chfle)
