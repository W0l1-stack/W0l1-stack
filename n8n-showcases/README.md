# n8n automation engineering showcases

These are **public, sanitized demonstrations** of automation architecture and examples from Williams Olawale's workflow engineering work.

[↩ GitHub profile](../README.md) · [Portfolio](https://wolistack.base44.app) · [Interactive portfolio](https://wolistack.olawalew345.chatgpt.site)

## Projects

| Showcase | What it demonstrates | What is published |
| --- | --- | --- |
| [Financial Intelligence Agent](financial-intelligence-agent.md) | Financial intent understanding, transaction processing, commands, review, records, reporting, and guardrails across a large production n8n workflow | Architecture case study only |
| [Financial Dashboard Reporting Sync](financial-dashboard-sync.md) | Five-minute reporting mart synchronization, PostgreSQL aggregation and dashboard read model | Case study and **sanitized, importable reference structure** |
| [WhatsApp-to-Finance Bridge](whatsapp-finance-bridge.md) | WhatsApp intake, normalization, identity routing, financial engine reuse, deduplication and response delivery | Architecture case study only |
| [Finance Snapshot Demo](templates/finance-snapshot-demo.json) | Currency-safe, deterministic financial summaries in n8n without any external credentials | **Importable, self-contained demo** |

### Real workflow sizes

The connected n8n workspace contains the active **Financial Intelligence Agent (264 nodes)** and **Financial Dashboard Reporting Sync (7 nodes)**. The WhatsApp finance connector currently has **17 nodes**, but is inactive in the connected instance. Node counts are snapshots from 22 October 2026 and may change.

## Try the demo

1. Open n8n, create a new workflow, and import [`templates/finance-snapshot-demo.json`](templates/finance-snapshot-demo.json) from file.
2. Select **Manual Trigger** and execute the workflow.
3. Inspect the output. Sample Nigerian naira and US dollar transactions remain in **separate currencies**; the demo deliberately avoids inventing exchange rates.

This demonstration intentionally contains **no API credentials, personal identifiers, database URLs, webhook addresses, live provider configuration, or customer records**. It does not sync a real financial database. The reporting-sync redacted reference likewise requires you to configure your own database, query, and destination before it can be run.

### What is intentionally omitted

Production code nodes, SQL functions and queries, API payload mappings, encryption and authorization logic, customer/account IDs, phone numbers, credentials, secrets, domain endpoints, tokens, and deployment configuration. A public repository is not the place to publish a live client's operating system.

**Security:** never import the sanitized reporting reference into a live environment and activate it without supplying and validating your own data source, security permissions and endpoint.
