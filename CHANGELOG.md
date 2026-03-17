# Meshly Changelog

All notable changes to Meshly are documented here.

---

## v1.0.0 — March 2026

### New Features

- **User Impersonation (Admin)** — Meshly staff can securely view a customer's workspace to assist with support, with full audit logging of every impersonation session
- **Meshly Validate** — Upload contracts and validate them against your organization's rules; results include severity ratings and remediation guidance
- **Meshly Intelligence** — Drift detection and cross-source intelligence hub for continuous contract and revenue monitoring
- **AI Query Agent** — Ask natural language questions about your contracts and receive cited, auditable answers
- **Reports** — Filter and export contract data across your organization
- **Role-Based Access Control** — Granular permissions across 12 roles including `customer_admin`, `customer_auditor`, `read_only`, and more

### Security & Compliance

- Log injection fixes — sanitized user-controlled values in log statements across API routes
- Firestore tenant isolation — enforced `org_id`/`tenant_id` filters on all cross-tenant queries
- Dependency CVE patches — bumped PyJWT ≥ 2.12.1, pypdf ≥ 6.9.0
- Fixed filenames with spaces in GCS signed URL generation (URL-encode path segments)
- Improved session expiry messaging — users see clear prompts when their session has expired

### Infrastructure

- GCP VPC network with VPC Flow Logs enabled (SOC 2 CC6.6)
- Structured JSON logging with OpenTelemetry trace propagation
- Audit event schema with `customer_id`/`tenant_id` isolation for every event
- KMS, rate-limit, and WebSocket auth audit events
- W3C `traceparent` propagation via trace context middleware

### Integrations

- Salesforce, DocuSign, Google Drive, QuickBooks, NetSuite, and Microsoft Dynamics connectors available

---

*Meshly is SOC 2 Type II in progress. Security information: [Vanta Trust Center](https://app.vanta.com/meshly.ai/trust/b667n0dd22c1b8xg5yqvf8)*
