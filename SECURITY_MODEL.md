# Security model — web-slide-fps

This is the threat model used by Devin security scans. It is shared across pzzp5252's five repositories (claude-code-sourcemap, dji-remote-c3, hvac-validation-docs, opencode-gmp-skills, web-slide-fps), which are unrelated systems scanned separately. This file covers **web-slide-fps**. Facts marked **(owner)** come from the repository owner; the rest is read from the code. No infrastructure repository exists: these are local tools, firmware and research code, nothing hosted **(owner)**.

## Components

| Component | Code | Trust boundary |
|---|---|---|
| FPS-Prototype | Only `README.md` today | Planned browser client + Geckos.io WebRTC server |

## System overview

Planned browser FPS prototype (TypeScript, Three.js, Rapier3D, Geckos.io/WebRTC, Vitest). The repository currently contains only the README. Kept in scans despite having little code **(owner)**.

## What will matter once code exists (inferred)

- The multiplayer server must treat client input as untrusted (server-authoritative movement and hit resolution).
- Supply chain: npm dependencies.

## Owner priorities across all repositories

- Integrity of GMP validation records and reports (data integrity, ALCOA+) **(owner, critical)**.
- Camera control and take/journal integrity in the field **(owner, critical)**.
- Developer/QA workstations that run these tools **(owner)**.

## Finding tags

- `Component` (table above), `CVE` for known dependency vulnerabilities, `GMP-relevance` = yes when the finding could affect GMP record/report or data integrity (ALCOA+), otherwise no **(owner)**.
