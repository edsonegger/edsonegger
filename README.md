## Edson Egger

Software engineer in Edmonton, Alberta. Twenty years building backend systems — the last four and a half on endpoint security at Rapid7, working in Python and Go across an agent fleet of 15M+ assets in 11 regions.

Most of what I've built lives in private repositories: agent internals, package signing and integrity, certificate and token issuance. What that work looks like —

**Protocol migration at fleet scale.** Moved the agent and all backend connection paths from TLS 1.0 to TLS 1.2+ across 15M+ assets. Backward-compatible negotiation with a phased, region-by-region rollout, because a failed handshake on a remote agent isn't recoverable without physical access.

**Software distribution integrity.** Replaced a legacy bash-script installer with native `.deb` / `.rpm` / `.pkg` packages, added integrity checks preventing package overwrites, and hardened file permissions. The orchestrator signature-checks every package before installation, stages new versions into isolated versioned directories, and activates them by atomic symlink swap with rollback on failed startup.

**Certificate and token issuance.** Rebuilt the service that authenticates every agent binary and file on customer machines — Python 2.7 on Lambda to Java 11 + Spring on Kubernetes — because FIPS compliance had to hold at the runtime level, not only in transport. Independently audited by the U.S. federal government rather than self-certified.

**Runtime and dependency remediation.** Python 3.14, OpenSSL 3.6 and Go 1.26 uplifts across ARM64/AMD64 on Windows, Linux and macOS, with multi-architecture `docker-bake` builds and base image migrations to remove end-of-life components.

Before that, fourteen years on mission-critical public-sector systems in Brazil — national passport and visa issuance with biometric and RFID hardware, the platform behind the 190 police emergency line, payroll lending at ~32.5M loans/day.

**Working in:** Python · Go · Java/Spring · Kubernetes · Terraform · AWS · OpenSSL

Currently looking at product security and platform engineering roles.

[LinkedIn](https://linkedin.com/in/edson-edgar-egger)

<!--
**edsonegger/edsonegger** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
