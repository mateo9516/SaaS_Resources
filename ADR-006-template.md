# ADR-006 — Multitenancy and Data Strategy

- **Status:** Proposed
- **Date:** YYYY-MM-DD

## Context

Describe the SaaS customer model, expected number/type of tenants, data sensitivity, growth expectations and operational constraints.

## Tenant model

- Tenant definition:
- Can a user belong to multiple tenants?:
- Membership model:
- Tenant context resolution:

## Access model

- Tenant-scoped roles:
- Important permissions:
- Feature flags:
- Entitlements:
- Tenant configuration:

## Data classification

| Data | Category | Notes |
|---|---|---|
| | Global / Tenant-owned / Tenant-config / Aggregated / Sensitive | |

## Alternatives considered

### A. Shared database / shared schema

Benefits:

Costs/risks:

### B. Shared database / schema per tenant

Benefits:

Costs/risks:

### C. Database per tenant

Benefits:

Costs/risks:

### D. Hybrid

Benefits:

Costs/risks:

## Decision

Selected strategy:

Why:

## Isolation rules

- Tenant-scoping rule:
- Unique constraints:
- Index strategy:
- Defense-in-depth controls:

## Migration strategy

Describe how schema changes are rolled out, tracked and recovered.

## Growth / noisy-neighbor strategy

Describe what happens when one tenant grows substantially.

## Consequences

### Positive

- 

### Negative

- 

## Review triggers

Revisit this ADR when any of the following becomes true:

- a tenant exceeds defined workload thresholds;
- compliance requires dedicated storage;
- restore or residency requirements change;
- migration time/complexity becomes unacceptable;
- noisy-neighbor incidents become material.
