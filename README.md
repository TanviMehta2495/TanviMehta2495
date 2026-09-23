<!--
  HOW TO USE: create a public repo named exactly TanviMehta2495 (same as your username).
  Upload this README.md and the assets/ folder. GitHub shows it on your profile automatically.
  Swap each photo placeholder in assets/photos/ for a real .jpg and update the link.
-->

<p align="center">
  <img src="assets/banner.svg" alt="Tanvi Mehta, Site Reliability Engineer" width="100%"/>
</p>

<p align="center">
  <a href="https://linkedin.com/in/tanvimehta2495"><img src="https://img.shields.io/badge/LinkedIn-tanvimehta2495-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <img src="https://img.shields.io/badge/AWS-Solutions%20Architect%20Associate-FF9900?style=for-the-badge&logo=amazonwebservices&logoColor=white" alt="AWS Certified Solutions Architect Associate"/>
  <img src="https://img.shields.io/badge/UT%20Dallas-MS%20ITM%20'27-E87500?style=for-the-badge" alt="UT Dallas MS ITM 2027"/>
  <img src="https://img.shields.io/badge/Dallas,%20TX-Open%20to%20SRE%20%2F%20Cloud%20roles-2dd4bf?style=for-the-badge" alt="Open to SRE and Cloud roles"/>
</p>

> **Most people only notice reliability when it breaks.**
> I've spent seven years making sure they don't have to.

---

<p align="center">
  <img src="assets/timeline.svg" alt="Timeline: 2017 B.E. at NMIT, 2017–21 Infosys, 2021–25 Lowe's, 2025 move to Dallas, 2026 UT Dallas, 2027 graduation" width="100%"/>
</p>

## 📖 Chapter 1 · Roots

<img src="assets/photos/roots.svg" alt="College days at NMIT" width="42%" align="right"/>

It started in Karnataka, with a **B.E. in Information Science and Engineering** from Nitte Meenakshi Institute of Technology (2017).

Back then, "production" was just a word in a textbook. I didn't know yet that I'd spend my career on the part of software nobody sees: the part that has to stay up while everyone is using it.

<!-- ✍️ Add one line in your own words: what first pulled you into engineering? -->

<br clear="right"/>

## 🛠️ Chapter 2 · Learning that production is personal

**Infosys · Senior Systems Engineer · 2017–2021**

My first real system was high-volume **credit-card infrastructure for BP**. When a card system fails, a real person at a real fuel pump can't pay. That changes how you debug.

- Debugged .NET production issues and resolved critical incidents **within SLA**
- Wrote PowerShell health checks and monitoring automation, **cutting manual toil by 30%**

The lesson I carried forward: *if you have to do it twice by hand, automate it.*

## 🔥 Chapter 3 · The Black Friday years

**Lowe's · Senior Software Engineer (SRE) · 2021–2025**

<p align="center">
  <img src="assets/black-friday.svg" alt="Load-test capacity vs. Black Friday traffic peak, with impact stats: $880K savings, 80K+ daily jobs, 40% faster tests, 50% less toil" width="100%"/>
</p>

At one of the largest US home-improvement retailers, the calendar revolves around **Tier-1 events** like Black Friday and Cyber Monday. The job was simple to say and hard to do: *be ready before the traffic arrives.*

- 🧪 Designed and ran **load tests simulating peak-year traffic** to find bottlenecks and validate capacity *before* the big day
- 💸 Led the **Cavisson → K6** performance-testing migration: **$880K in annual savings** and **40% faster test runs**
- ⚙️ Built and ran CI/CD pipelines powering **80,000+ job executions a day**
- 🤖 Wrote Groovy and Bash auto-recovery for common pipeline failures, **cutting manual toil by 50%**
- 📊 Built a **React dashboard with a custom data pipeline** tracking Core Web Vitals, which caught regressions early and drove quarter-over-quarter speed gains

And then there were the nights.

<p align="center">
  <img src="assets/oncall-terminal.svg" alt="Illustrated on-call terminal: page, investigate in Grafana and ELK, resolve, write postmortem, automate" width="100%"/>
</p>

As part of a **24/7 SRE on-call rotation**, I watched services against their SLOs in **Grafana and ELK**. I led root-cause analysis and wrote blameless postmortems whose action items **reduced repeat incidents and MTTR**.

<img src="assets/photos/bangalore.svg" alt="Bangalore work life" width="60%"/>

## ✈️ Chapter 4 · The leap

<p align="center">
  <img src="assets/journey-map.svg" alt="Animated flight path from Bangalore to Dallas, about 14,900 km" width="100%"/>
</p>

After seven years, I chose to **reset on purpose**. I left a senior role in Bangalore to start an **M.S. in Information Technology and Management at UT Dallas (JSOM)**, where I hold a **3.9 GPA**.

I didn't come to start over. I came to go deeper into cloud architecture, data engineering and AI systems, and to learn how to *design* systems, not just keep them alive.

<!-- ✍️ Add one honest line: what did it feel like to make this move? -->

<img src="assets/photos/dallas.svg" alt="Arriving at UT Dallas" width="60%"/>

## ☁️ Chapter 5 · Building from zero on AWS

**UT Dallas · Student Assistant · Feb–May 2026**

This time I wasn't inheriting infrastructure. I **designed it from scratch** for a production driver web app, all defined in **AWS CDK (TypeScript)**.

<p align="center">
  <img src="assets/aws-architecture.svg" alt="AWS architecture: CloudFront and S3 for React, App Runner backend in a VPC, RDS and MongoDB, Secrets Manager, CodePipeline, CloudWatch" width="100%"/>
</p>

- React frontend on **S3 + CloudFront**, backend on **AWS App Runner**
- Two databases, each for what it does best: **RDS** for transactional records, **MongoDB** for flexible documents
- Locked down with **VPC isolation, IAM roles and Secrets Manager**
- Shipped through **CodePipeline** and observed with **CloudWatch**, because old SRE habits die hard 😄

## 🤖 Chapter 6 · Teaching a pipeline to learn

### [AiOcr: AI-Powered Data Quality Platform for Unstructured Data](https://github.com/TanviMehta2495/AiOcr)

Businesses drown in PDFs. LLMs can read them, but calling an LLM for *every* document is slow and expensive. So I asked a reliability question:

> *What if the system remembered every layout it had already learned?*

<p align="center">
  <img src="assets/aiocr-pipeline.svg" alt="AiOcr pipeline: upload, parse, layout signature, template memory or rules plus LLM, validate, human review, store, and a learning loop back to template memory" width="100%"/>
</p>

- 🧠 **Template memory** fingerprints each document's layout. Known layouts are extracted **without an LLM call**. New ones fall back to rules plus LLM-assisted extraction with strict JSON output.
- ✅ **Validation** checks required fields, dates and totals, and a **human-in-the-loop review** screen shows the PDF side by side with the extracted data.
- 🔁 **It learns without fine-tuning.** Approved results feed back into template memory, so repeat documents get faster and cheaper over time.
- 🚀 Built like production: Streamlit UI, Docker, **GitHub Actions CI** (Python 3.11/3.12 matrix), **dev → test → main** promotion and a workflow for promoting learned artifacts between environments
- 💾 Outputs to **JSON, CSV, SQLite** and extraction trace logs

`Python` `Streamlit` `pdfplumber` `LLMs` `SQLite` `Docker` `GitHub Actions`

➡️ **[Explore the repo](https://github.com/TanviMehta2495/AiOcr)**

## 🌱 Chapter 7 · What's next

<img src="assets/photos/today.svg" alt="Tanvi today" width="38%" align="right"/>

I graduate in **May 2027**, and I'm looking for **Site Reliability, Cloud and Platform Engineering** roles where I can bring:

- 7+ years of production instincts: SLOs, on-call, postmortems, capacity planning
- Hands-on AWS architecture, backed by the **Solutions Architect – Associate** certification
- A builder's curiosity for **AI systems that are reliable**, not just impressive

If your systems can't afford to go down, let's talk. 👋

<br clear="right"/>

---

## 🧰 Toolbox

| | |
|---|---|
| **Reliability** | SLIs/SLOs · Incident Response · Postmortems & RCA · On-Call · Toil Reduction |
| **Performance** | K6 · Cavisson · Load & Stress Testing · Capacity Planning · Core Web Vitals |
| **Observability** | Grafana · ELK Stack · AWS CloudWatch |
| **Cloud** | AWS (EC2, S3, VPC, IAM, ALB, App Runner, CloudFront, Lambda, CDK, RDS, Secrets Manager) |
| **CI/CD & Containers** | Jenkins · GitHub Actions · AWS CodePipeline · Docker · Kubernetes (EKS) |
| **Code & Data** | Python · TypeScript · JavaScript · Bash · Groovy · SQL · MongoDB · SQLite · React |

<p align="center">
  <img src="https://skillicons.dev/icons?i=aws,kubernetes,docker,githubactions,jenkins,grafana,elasticsearch,python,ts,js,bash,react,mongodb,sqlite&perline=14" alt="Tech icons"/>
</p>

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=TanviMehta2495&show_icons=true&theme=tokyonight&hide_border=true" height="160" alt="GitHub stats"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=TanviMehta2495&layout=compact&theme=tokyonight&hide_border=true" height="160" alt="Top languages"/>
</p>

<p align="center"><i>Keeping systems up, and always learning. 🟢</i></p>
