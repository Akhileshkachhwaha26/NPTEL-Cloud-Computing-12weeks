# ☁️ NPTEL Cloud Computing – Assignment Solutions

Solutions to the weekly assignments (Weeks 1–12) of the **NPTEL Cloud Computing** course offered by **IIT Kharagpur**. Each assignment has 10 MCQ/MSQ questions (10 marks), and the repository contains the question papers with the correct answers and detailed explanations.

> ⚠️ **Disclaimer:** This repository is for revision and learning only. Assignment questions can change between course sessions, so attempt the questions yourself first and use these solutions to check your understanding and read the reasoning. This is not an official NPTEL or IIT Kharagpur resource.

---

## 📚 Topics Covered

| Week | Main Topics |
|:----:|-------------|
| 1 | Cloud fundamentals, resource pooling, IaaS/PaaS/SaaS/XaaS, deployment models, virtualization basics, distributed systems, grid vs. cluster |
| 2 | Para-virtualization vs. full virtualization, public cloud, XML parsers (SAX/StAX/DOM), host/guest OS & hypervisor, SOAP, WSDL, UDDI, SOA publish–find–bind |
| 3 | Cloud SLAs (multilevel SLA, availability, MTTR, RTO), parallel databases, stream processing (Kafka/Flink/Kinesis), object storage, MapReduce combiner, OpenStack CPU allocation ratio |
| 4 | Azure (SQL Hyperscale, Availability Zones, App Service), GCP (Cloud Spanner, GKE vs. Cloud Run, Pub/Sub + BigQuery, App Engine traffic splitting), OpenStack (Cinder, Neutron) |
| 5 | SLA downtime calculation, power consumption, pay-as-you-go, HDFS/MapReduce (partitioner, combiner), energy-aware scheduling, elasticity, utility-premium cost analysis |
| 6 | CIA triad, authenticity, active vs. passive attacks, DoS, reconnaissance, authentication vs. authorization, cloud security concerns, vendor lock-in |
| 7 | Mobile Cloud Computing, computation offloading, cloudlets, fog computing, geospatial cloud computing, IoT healthcare architecture |
| 8 | Docker commands, VMs vs. containers, Kubernetes etcd, Type-1/Type-2 hypervisors, VM consolidation, Sensor Cloud middleware, Edge/Fog–Cloud |
| 9 | Edge–Fog–Cloud hierarchy, vertical vs. horizontal scalability, mobility and service migration, cloud federation, trust management, hybrid cloud federation |
| 10 | Live VM migration (pre-copy / post-copy), fog load balancing, kube-scheduler, Dockerfile → image → container, namespaces & cgroups, Docker volumes |
| 11 | Dew computing, offline sync and conflict resolution, serverless/FaaS, cold start, stateless functions, Lambda timeout limits, Amazon Redshift |
| 12 | Mobile Cloud Computing, spatial cloud computing, Cyber-Physical Systems, spatial trajectories & crowdsourcing, V2V, connected vehicles, 5G (eMBB) |

---

## ✅ Quick Answer Key

| Week | Q1 | Q2 | Q3 | Q4 | Q5 | Q6 | Q7 | Q8 | Q9 | Q10 |
|:----:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:---:|
| 1  | B | C | D | B | A | C | B | A | B | B |
| 2  | C | B | B | C | B | D | B | A | B | A |
| 3  | B | D | C | A | A | B | C | B | B | B |
| 4  | C | B | C | C | C | C | C | B | A | B |
| 5  | A | C | B | B | B | B | C | B | A | A |
| 6  | B | D | C | C | B | C | B | C | A | B |
| 7  | C | B | B | B | B | B | C | A | B | B |
| 8  | B | A | B | B | C | B | B | B | A | A |
| 9  | B | C | A | D | B | C | B | A | A | C |
| 10 | B | C | B | C | B | B | B | B | B | C |
| 11 | B | C | B | B | B | C | B | B | B | A |
| 12 | A | B | B | B | A | B | B | C | B | A |

---

## 📝 Worked Calculations

A few numerical questions come up repeatedly, so here are the formulas used.

**SLA downtime (Week 3, Q5)**
`Allowed downtime = (1 − availability) × total time = 0.001 × 720 h = 0.72 h ≈ 43 min`

**SLA downtime for a partial-day workload (Week 5, Q1)**
`Operating time = 12 h × 30 days = 360 h → 0.01 × 360 = 3.6 h`

**OpenStack vCPU overcommit (Week 3, Q10)**
`Allocatable vCPUs = physical vCPUs × allocation ratio = 640 × 5 = 3200`

**HDFS map tasks (Week 5, Q4)**
`⌈700 MB / 128 MB⌉ = ⌈5.47⌉ = 6 map tasks (one per block)`

**Cloud vs. owning cost (Week 5, Q10)**
Break-even premium = peak ÷ average = 225 ÷ 75 = 3. The provider's premium is 2.8, which is below 3, so the cloud is cheaper.

**Cold VM migration time (Week 10, Q8)**
`(32 × 2³⁰) / (16 × 2²⁰) = 2048 s ≈ 34 minutes`

---

## 🗂️ Repository Structure

```
.
├── README.md
├── Assignment_1.pdf
├── Assignment_2.pdf
├── ...
├── Assignment_11.pdf
└── Assignment_12.pdf
```

Each PDF contains:
- the question and its options
- the **correct answer**
- a **detailed solution** explaining why the answer is right and why the others are wrong

---

## 🚀 How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/<repo-name>.git
   cd <repo-name>
   ```
2. Open the PDF for the week you want to review.
3. Try the questions first, then compare your answers with the key above.
4. Read the detailed solutions for anything you got wrong.

---

## 🧠 Key Concepts Cheat Sheet

- **Service models:** SaaS (use the app) → PaaS (deploy code) → IaaS (manage OS and above) → FaaS (deploy functions).
- **Deployment models:** Public, Private, Community, Hybrid.
- **Hypervisors:** Type 1 (bare-metal: ESXi, Xen, Hyper-V Server). Type 2 (hosted: VirtualBox, VMware Workstation).
- **Containers vs. VMs:** Containers share the host kernel; VMs run their own guest OS kernel.
- **Edge vs. Fog vs. Cloud:** Edge handles immediate local action, Fog handles regional aggregation and coordination, and Cloud handles global analytics, storage and training.
- **Live migration:** Pre-copy sends memory first and then switches over. Post-copy switches first and fetches pages on demand.
- **Passive attacks:** Sniffing, eavesdropping, traffic analysis. Active attacks: hijacking, replay, MITM, masquerading, DoS.
- **Serverless:** Stateless, scales horizontally, and has cold starts and execution time limits (AWS Lambda: 15 min).
- **5G categories:** eMBB (high bandwidth), URLLC (ultra-low latency), mMTC (massive IoT).

---

## 🤝 Contributing

Found a mistake or have a better explanation? Open an issue or send a pull request.

## ⭐ Support

If this repository helped you, consider giving it a star.

## 📄 License

Shared for educational purposes. All course content and questions belong to **NPTEL / IIT Kharagpur**.
