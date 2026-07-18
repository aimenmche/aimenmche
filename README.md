<div align="center">

  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&pause=1000&color=00FF88&center=true&vCenter=true&width=500&lines=Hey%2C+I'm+Aimen;Security+Enthusiast+%E2%9A%A1;I+break+things+to+understand+them;Building+tools+that+catch+attackers" alt="Typing SVG" />

  <p>
    <a href="https://github.com/dzdzdzdzdzdz213/beacon-guard"><img src="https://img.shields.io/badge/BeaconGuard-eBPF_Kernel_Guard-00FF88?style=flat-square&logo=linux&logoColor=white" /></a>
    <a href="https://github.com/dzdzdzdzdzdz213/k8s-runtime-guard"><img src="https://img.shields.io/badge/K8s_Runtime_Guard-Container_Security-58A6FF?style=flat-square&logo=kubernetes&logoColor=white" /></a>
    <a href="https://github.com/dzdzdzdzdzdz213/cloudsweep"><img src="https://img.shields.io/badge/CloudSweep-CSPM_Scanner-FF6B6B?style=flat-square&logo=amazonaws&logoColor=white" /></a>
    <a href="https://github.com/dzdzdzdzdzdz213/watchtower"><img src="https://img.shields.io/badge/WatchTower-SIEM-58A6FF?style=flat-square&logo=datadog&logoColor=white" /></a>
    <a href="https://github.com/dzdzdzdzdzdz213/cloudsec-pipeline"><img src="https://img.shields.io/badge/CloudSec_Pipeline-OPA%2FRego-7B2FF7?style=flat-square&logo=openpolicyagent&logoColor=white" /></a>
    <a href="https://github.com/dzdzdzdzdzdz213/cybersec-journey"><img src="https://img.shields.io/badge/Cybersec_Journey-50_Tools-FF6B6B?style=flat-square&logo=python&logoColor=white" /></a>
    <img src="https://komarev.com/ghpvc/?username=dzdzdzdzdzdz213&style=flat-square&color=00FF88" />
  </p>

</div>

---

I'm fascinated by how systems break. Not a security engineer — just someone who obsesses over kernel hooks, network exploits, and the cat-and-mouse game between attackers and defenders. I build tools to learn how attacks work, then share them so others can learn too.

Currently exploring: **eBPF behavioral detection**, **cloud misconfigurations**, **network forensics**, and **red team automation**.

---

## What I've Been Building

### [BeaconGuard — eBPF Behavioral Kernel Guard](https://github.com/dzdzdzdzdzdz213/beacon-guard)
Real-time process anomaly detection — no signatures, no static rules, just pure behavioral analysis. Hooks 9 kernel syscalls, builds per-process baselines, kills what looks wrong.

```
execve, openat, tcp_connect, mmap, ptrace  ──▶  behavioral engine  ──▶  kill anomalies
```
- Detects C2 beaconing by analyzing connection interval variance
- Finds reverse shells, DNS tunneling, mass file deletion, sensitive writes
- Learning mode builds normal behavior profile → enforcement mode catches deviations

---

### [K8s Runtime Guard — Container Escape Detection](https://github.com/dzdzdzdzdzdz213/k8s-runtime-guard)
When a container tries to escape to the host, this catches it. 9 eBPF hooks monitoring namespace boundaries, cgroup manipulation, and mount syscalls.

- Catches CVE-2022-0492 (cgroup release_agent) in real time
- Detects cross-namespace ptrace, shell spawning, fork bombs
- Correlates with Kubernetes audit logs for full context

---

### [WatchTower — SIEM for the Rest of Us](https://github.com/dzdzdzdzdzdz213/watchtower)
A security dashboard that actually makes sense. Ingest SSH logs, Nginx logs, JSON payloads — it figures out the format and runs detection rules against everything.

- 7 detection rules: brute force, SQLi, port scans, off-hours logins
- Real-time WebSocket alerts streaming to a dark-themed dashboard
- Alert deduplication so you don't get alert storms

---

### [CloudSweep — AWS Misconfiguration Scanner](https://github.com/dzdzdzdzdzdz213/cloudsweep)
50+ security checks across S3, EC2, IAM, KMS, CloudTrail, RDS, Lambda, VPC, and GuardDuty. Because half of cloud breaches start with a misconfigured S3 bucket.

---

### [CloudSec Pipeline — Policy as Code](https://github.com/dzdzdzdzdzdz213/cloudsec-pipeline)
OPA/Rego policies that block insecure Terraform and Kubernetes configs before they reach production. GitHub Actions integration + ArgoCD enforcement.

---

### [ShieldWall — Network IDS](https://github.com/dzdzdzdzdzdz213/cybersec-journey/tree/master/shieldwall)
Real-time network traffic monitoring with plugin-based detection, MITRE ATT&CK mapping, and a React dashboard. Elasticsearch + Kibana output included.

---

### [Cybersec Journey — 50 Security Tools](https://github.com/dzdzdzdzdzdz213/cybersec-journey)
A collection of 50 tools I built while learning security. Packet sniffers, C2 frameworks, forensics tools, cryptanalysis, OSINT — everything a curious mind needs.

| What | Tools |
|------|-------|
| Network | Sniffer, DNS tunnel, honeypot, port knocker |
| Crypto | Steganography, ZK proofs, cipher cracker |
| Forensics | Disk imager, file carver, memory analysis |
| Red Team | C2 server, payload generator, lateral movement |
| Web | SQLi toolkit, XSS sandbox, JWT inspector |

---

## How I Think About Security

> I don't just want to defend against attacks — I want to understand them deeply enough to build tools that catch what others miss.

Every project starts the same way: **how would an attacker do this?** Then I build the detector, the hard way, from scratch. No frameworks doing the thinking for me.

---

## Toolchain

```
Kernel        C · eBPF · libbpf
Systems       Go · Rust · Assembly
Backend       Python · FastAPI · Flask
Frontend      React · Recharts · WebSocket
Infra         Docker · Kubernetes · Terraform · OPA
Storage       PostgreSQL · SQLite · Elasticsearch
```

---

<div align="center">

  <a href="https://github.com/dzdzdzdzdzdz213">
    <img height="160em" src="https://github-readme-stats.vercel.app/api?username=dzdzdzdzdzdz213&show_icons=true&theme=dark&hide_border=true&include_all_commits=true&count_private=true&bg_color=0D1117" />
    <img height="160em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=dzdzdzdzdzdz213&layout=compact&theme=dark&hide_border=true&langs_count=8&bg_color=0D1117" />
  </a>

  <br />

  <a href="https://github.com/dzdzdzdzdzdz213/beacon-guard">
    <img src="https://github-readme-stats.vercel.app/api/pin/?username=dzdzdzdzdzdz213&repo=beacon-guard&theme=dark&hide_border=true&bg_color=0D1117&description_lines_count=1" />
  </a>
  <a href="https://github.com/dzdzdzdzdzdz213/watchtower">
    <img src="https://github-readme-stats.vercel.app/api/pin/?username=dzdzdzdzdzdz213&repo=watchtower&theme=dark&hide_border=true&bg_color=0D1117&description_lines_count=1" />
  </a>
  <a href="https://github.com/dzdzdzdzdzdz213/cybersec-journey">
    <img src="https://github-readme-stats.vercel.app/api/pin/?username=dzdzdzdzdzdz213&repo=cybersec-journey&theme=dark&hide_border=true&bg_color=0D1117&description_lines_count=1" />
  </a>

</div>

---

<div align="center">

  *Curious mind. Building security tools because I can't stop asking "how would I break this?"*

  <a href="mailto:aimenmamache0@gmail.com"><img src="https://img.shields.io/badge/Email-aimenmamache0%40gmail.com-00FF88?style=flat-square&logo=gmail&logoColor=white" /></a>
  <a href="https://github.com/dzdzdzdzdzdz213"><img src="https://img.shields.io/badge/GitHub-dzdzdzdzdzdz213-00FF88?style=flat-square&logo=github&logoColor=white" /></a>

</div>
