# DataHub Supplier Data Lineage Governance Platform
## The Problem
Supplier data cannot be trusted when source lineage is unclear, ownership reviews are skipped, and certification decisions are undocumented.
## The Solution
This platform governs supplier data asset registration, lineage review, certification, and accountable audit evidence.
## Live Demo & Tech Stack
The service binds to `0.0.0.0:20800`. The stack uses Node.js, DataHub-oriented lineage governance patterns, Express, Vitest, and GitHub Actions.
## Local Setup & Run Instructions
```bash
npm install
npm test
npm start
```
## System Documentation (Mermaid.js)
### System Architecture Diagram
```mermaid
flowchart LR
  Engineer-->Lineage[Data lineage service]
  Owner-->Lineage
  Manager-->Lineage
  Lineage-->Audit[Audit events]
```
### Entity-Relationship Diagram
```mermaid
erDiagram
  DATA_ASSET ||--o{ AUDIT_EVENT : records
  DATA_ASSET { string id string supplier string source string state }
  AUDIT_EVENT { string id string action string actor string role }
```
### Data Flow Diagram
```mermaid
flowchart TD
  Register-->Review-->Certify-->Audit
```
### Use Case Diagram
```mermaid
flowchart LR
  Engineer-->RegisterAsset
  Owner-->ReviewLineage
  Manager-->CertifyAsset
```
### Sequence Diagram
```mermaid
sequenceDiagram
  participant E as Engineer
  participant L as Lineage service
  participant M as Manager
  E->>L: Register asset
  L->>M: Submit reviewed lineage
  M-->>L: Certify asset
```
## Owner
Created and maintained by Kholipha Ahmmad Al-Amin.
Software Engineer and AI Specialist
Founder and CEO of EquiSaaS BD
Principal Consultant at AR IT Consultancy
Full Stack Developer and SaaS Product Builder
### Official links
Portfolio: https://kholipha-ahmmad-al-amin.equisaas-bd.com/
GitHub: https://github.com/kholipha-ahmmad-al-amin
LinkedIn: https://www.linkedin.com/in/kholipha-ahmmad-al-amin
X: https://x.com/al_amin5519
Facebook: https://www.facebook.com/kholipha.ahmmad.al.amin
Instagram: https://www.instagram.com/kholipha.ahmmad.al.amin
## Ownership
This project was created and is maintained by Kholipha Ahmmad Al-Amin.

