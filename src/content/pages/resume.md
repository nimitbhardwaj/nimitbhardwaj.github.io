---
title: "Resume"
description: "Nimit Bhardwaj: Senior Software Engineer, Backend & Infrastructure."
---

Senior Software Engineer · Backend & Infrastructure · Hyderabad, India

[Email](mailto:nimitbhardwaj@gmail.com) · [LinkedIn](https://www.linkedin.com/in/nimit-bhardwaj-b137a3116/) · [GitHub](https://github.com/nimitbhardwaj)

## Experience

### Lead, Tech: D. E. Shaw & Co. (July 2020 to present, Hyderabad)

- Technical owner of IRWeb, the firm's investor-facing platform serving ~10,000 investors daily with account balances, reports, document downloads, and conference-call video. Took it from the legacy stack to its current architecture and still run it in production.
- Designed and shipped integrations across four proprietary systems covering accounts, funds and feeders, transactions, balances, fees, contacts, and relationships. Bidirectional sync with the golden source, idempotent writes, reconciliation on every run.
- Built the central data-layer service that aggregates investor data from Arcesium and the upstream systems, normalizes it, and exposes it to downstream microservices with completeness checks before consumption.
- Designed and implemented a Python-JVM bridge (Py4J) so the modern Python/FastAPI stack could reuse business logic and document retrieval in the legacy Java codebase without a rewrite.
- Designed and coded a CRM used by the business end-to-end. Owned the HLD and LLD, built the APIs and business logic for every entity, consumed the ticket-management system's update stream to link tickets to the right CRM records, and exposed real-time account balance changes. Python backend, React frontend, two-year build with business stakeholders involved from day one.
- Own the HLD/LLD for a secure document-exchange portal extending IRWeb to two-way document sharing: investors and prospects upload, view, and share documents and converse directly with the business. Business reviewers annotate PDFs with draggable-region comments, and every conversation thread mirrors in parallel to email and syncs into the firm's internal ticketing system for business-side triage.
- Designed the document-security pipeline: uploads land in an S3 quarantine bucket, are scanned via AWS GuardDuty and peepdf (embedded-JS/exploit detection in PDFs), and a Lambda-triggered webhook promotes clean files to the production bucket or emails the investor on rejection.
- Extended portal access to prospects without an existing account via time-limited, passwordless magic-link email authentication.
- Designated Responsible Individual for IRWeb: on-call rotation, production monitoring, incident response, and root-cause analysis on customer-facing degradation. Wrote the runbooks the rotation uses.
- Own deployment: services containerized on Kubernetes via Helm, CI/CD pipelines, staged production cutover, and operational handoff.
- Work directly with Investor Relations, Operations, and InfoSec to turn requirements into architecture, and surface scope changes and risks early rather than absorbing them silently.

### Software Developer Intern: Codehall (May 2019 to Mar 2020, remote)

- Built an online code-execution judge in Python supporting C, C++, Java, JavaScript, and Python, with sandboxed compile-and-run, resource limits and result validation.
- Built the judge's REST backend in Django with Celery for async job orchestration, Redis for queueing, Docker for sandbox isolation, and Ansible for deployment.

## Skills

- **Languages:** Python, TypeScript, JavaScript, C++, C, Java, Rust, SQL, Bash
- **Backend:** FastAPI, Django, Flask, Pydantic, Celery, SQLAlchemy, REST, JSON-RPC, WebSocket, OAuth, HMAC request signing, mTLS, Py4J, passwordless / magic-link auth
- **Data:** PostgreSQL, MySQL, MongoDB, Redis, NumPy, Pandas
- **Frontend:** React, Redux, TypeScript, Webpack
- **Cloud & Infrastructure:** Kubernetes, Helm, Docker, Podman, AWS Lambda, AWS Cognito, AWS EC2, AWS S3, AWS GuardDuty, peepdf, Cloudflare Workers, Tailscale, Nginx, Caddy, Linux
- **Practices:** System design (HLD/LLD), API contract design, idempotency and retry semantics, observability, CI/CD, on-call / DRI, pytest, code review
- **AI / LLM:** Production LLM API integration, AI-augmented development workflows

## Projects

- **[tunnelterm](https://github.com/nimitbhardwaj/tunnelterm)** (PyPI): FastAPI server that spawns a real PTY and bridges it to the browser over WebSocket. RFC 6238 TOTP, HttpOnly SameSite cookies, fail-closed Origin allow-list, trusted-proxy X-Forwarded-For, LRU token store with TTL, per-IP rate limiting, sticky sessions with ring-buffer replay. CI and release pipeline.
- **[dotman](https://github.com/nimitbhardwaj/dotman-cli)** (PyPI): Dotfile manager on symlinks and Jinja2 templates. Package dependency graph with circular-dependency detection, machine-specific overrides, dry-run, pre/post-deploy hooks, deployment history with rollback, watch mode, remote git sync. 31 test modules.
- **[shellr](https://github.com/nimitbhardwaj/shellr)**: Control a rooted Android phone from a VPS over Tailscale. HMAC-signed JSON-RPC, pure-stdlib daemon bound to the tailnet interface only, allow-listed paths, kernel-resident autostart via KernelSU.

## Education

- **National Institute of Technology, Hamirpur** (2015 to 2020): Dual Degree M.Tech + B.Tech, Computer Science. 8.98 CGPA, Gold Medalist, Branch Topper.
- **D.A.V. Public School, Una** (2013 to 2015): Senior High School.

## Achievements

- Candidate Master (rating 1874), Codeforces
- Rank 35, Kharagpur Regionals 2019, ACM-ICPC
- Rank 70, Gwalior Regionals 2018, ACM-ICPC
- Gold Medalist, Branch Topper, NIT Hamirpur

## Open source

- Contributor to Mixxx and Neovim. Three self-authored Python packages published to PyPI.
