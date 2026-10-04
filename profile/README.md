<div align="center">

# Message Easy Mode

### Self-hosted Matrix + Element, made manageable.

**Message Easy Mode (MEM)** is an open-source control plane for deploying and operating self-hosted Matrix + Element communication servers without having to assemble every infrastructure component by hand.

[![Website](https://img.shields.io/badge/Website-messageeasymode.com-5B5BD6?style=for-the-badge)](https://messageeasymode.com/)
[![Documentation](https://img.shields.io/badge/Documentation-Read_the_docs-2F80ED?style=for-the-badge)](https://messageeasymode.com/docs)
[![Latest Release](https://img.shields.io/badge/Latest-0.2.0-00B894?style=for-the-badge)](https://github.com/message-easy-mode/mem-releases/releases/latest)
[![Source](https://img.shields.io/badge/Public_Source-GitHub-24292F?style=for-the-badge&logo=github)](https://github.com/message-easy-mode/mem)

</div>

---

## What is Message Easy Mode?

MEM brings the main operational pieces of a production-shaped Matrix deployment into one guided control plane.

Instead of managing Matrix, Element, TLS, TURN, backups, migration and operator tooling as separate systems, MEM gives you one place to install, configure, inspect and operate the platform.

### MEM 0.2.0 includes

| | Capability |
|---|---|
| 🧭 | Guided first-time platform setup and Platform Owner enrollment |
| 💬 | Matrix + Element chat-server lifecycle management |
| 🌐 | Domain management and DNS-backed TLS certificate workflows |
| 🔐 | Certificate issuance and renewal management |
| 📞 | Shared Coturn / TURN deployment and validation |
| 👥 | Matrix user administration |
| 💾 | Native backup, portable export, restore and recovery workflows |
| 🔄 | Migration tooling for supported legacy MEM installations |
| 🩺 | Diagnostics and operator support tooling |
| ⌨️ | Standalone `mem` operator CLI |
| 📚 | Embedded English and German operator documentation |

---

## Install Message Easy Mode

MEM 0.2.0 is qualified for:

```text
Ubuntu Server 24.04 LTS
amd64 / x86_64
Docker + Docker Compose
```

For a normal stable installation:

```bash
curl -fsSL https://messageeasymode.com/install.sh   -o /tmp/mem-install.sh && sudo bash /tmp/mem-install.sh
```

For deployment guidance, networking, DNS, certificates, TURN, backups, migration and troubleshooting, start with the [operator documentation](https://messageeasymode.com/docs).

---

## Designed for self-hosting

MEM is built for operators who want to own their infrastructure and data while reducing the amount of manual integration normally required to run a Matrix + Element service.

Typical deployments include:

- cloud VMs such as DigitalOcean;
- on-premises virtual machines;
- Proxmox-based environments;
- private administration over SSH tunnels;
- public Matrix, Element and TURN services behind a controlled network boundary.

Administrative surfaces such as the MEM Control Plane and Nginx Proxy Manager should remain private rather than being exposed directly to the public Internet.

---

## Current stable release

### Message Easy Mode 0.2.0

The 0.2.0 release includes a versioned installer, standalone CLI, MEM Migrate package, SPDX SBOM, release manifest and aggregate SHA-256 checksums.

**Release artifacts:**  
https://github.com/message-easy-mode/mem-releases/releases/latest

**Public source:**  
https://github.com/message-easy-mode/mem/tree/v0.2.0

**Control Plane image:**  

```text
ghcr.io/message-easy-mode/mem-control-plane:0.2.0
```

Release artifacts and the Control Plane image are tied to exact release identity and source provenance.

---

## Project repositories

### [`message-easy-mode/mem`](https://github.com/message-easy-mode/mem)

Release-aligned public source for Message Easy Mode, including:

```text
bootstrap/
cli/
dev/
installer/
migrate/
scripts/public-source/
scripts/release/
```

### [`message-easy-mode/mem-releases`](https://github.com/message-easy-mode/mem-releases)

Canonical release-artifact repository for:

- versioned installer bootstrap;
- installer bundle;
- standalone CLI;
- MEM Migrate release files;
- SPDX SBOM;
- `release.json`;
- `SHA256SUMS`.

---

## Release and source provenance

MEM deliberately keeps source publication, release artifacts and the runtime image as separate but linked surfaces:

```text
Public source
github.com/message-easy-mode/mem
        │
        ├── exact release source
        │
        ▼
Release artifacts
github.com/message-easy-mode/mem-releases
        │
        └── installer / CLI / Migrate / SBOM / checksums
        │
        ▼
Control Plane image
ghcr.io/message-easy-mode/mem-control-plane
```

This keeps the released source inspectable while allowing installers and runtime images to carry their own immutable release identity and verification metadata.

---

## Documentation

The public documentation covers:

- installation and first-time Setup;
- Matrix + Element server creation;
- domains and certificates;
- TURN and firewall requirements;
- user administration;
- backup and restore;
- migration;
- diagnostics;
- security and operator access.

**Read the docs:**  
https://messageeasymode.com/docs

---

## Security

Please do **not** report suspected security vulnerabilities through public issues or pull requests.

Use the private reporting process described in the [`SECURITY.md`](https://github.com/message-easy-mode/mem/blob/main/SECURITY.md) file.

---

## Open source

Message Easy Mode is released under the **GNU Affero General Public License v3.0 (AGPLv3)**.

Source, release artifacts and project documentation are published so operators can inspect the software they run and verify released builds against documented release provenance.

---

<div align="center">

### Own the server. Own the data. Make Matrix easier to operate.

[Website](https://messageeasymode.com/) ·
[Documentation](https://messageeasymode.com/docs) ·
[Latest Release](https://github.com/message-easy-mode/mem-releases/releases/latest) ·
[Public Source](https://github.com/message-easy-mode/mem)

</div>
