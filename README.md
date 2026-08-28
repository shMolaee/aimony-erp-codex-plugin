# Maian ERP for Codex

Maian ERP connects Codex to the user’s authenticated Maian workspace for permission-scoped reporting and governed ERP actions.

## Direct download

- [Download Maian ERP for Codex v0.2.9](https://dash.maian.app/downloads/standalone/codex/maian-erp/maian-erp-codex-plugin-v0.2.9.zip)
- [Download the latest package](https://dash.maian.app/downloads/standalone/codex/maian-erp/maian-erp-codex-plugin.zip)
- [SHA-256 checksum](https://dash.maian.app/downloads/standalone/codex/maian-erp/maian-erp-codex-plugin-v0.2.9.zip.sha256)

After downloading, extract the ZIP and add its root directory as a local Codex marketplace:

```powershell
codex plugin marketplace add C:\path\to\maian-erp-codex-plugin-v0.2.9
codex plugin add maian-erp@maian-erp
```

## Capabilities

- Identify the active workspace and keep all reads and writes tenant-scoped.
- Discover any currently authorized ERP capability through a compact, schema-versioned catalog even when the host reads only the first MCP tool page; reads, approval-gated writes, and internal records use disjoint effect lanes.
- Create, inspect, and revoke actor/workspace/source-bound standing approvals so explicitly authorized actions can execute without repetitive confirmation while critical actions and all domain safeguards remain protected.
- Count, filter, project, sort, and page ERP entities with opaque cursors.
- Follow declared one-hop relationships without bypassing target permissions.
- Create exact, replay-safe proposals and finalize one or several only after valid consent.
- Create tickets, add public replies or internal notes, and update ticket status.
- Start workflows and move instances through configured steps.
- Draft governed purchase invoices, payments, and balanced journals, then approve, post, or void exact version-checked finance documents.
- Create or update strategies, objectives, key results, KPIs, and risks through typed, version-checked tools.
- Read cataloged non-secret settings and update one allow-listed setting through the governed approval flow.
- Create, update, publish, or schedule blog posts through the governed approval flow.
- Guide sign-in through Codex without exposing OAuth, token, command-line, or transport details.

## Install from GitHub

Add this repository as a Codex plugin marketplace:

```powershell
codex plugin marketplace add shMolaee/maian-erp-codex-plugin
```

Then install the plugin:

```powershell
codex plugin add maian-erp@maian-erp
```

Open a new Codex task after installation. On first use, Codex starts the Maian sign-in flow. Each user authenticates against their own Maian account and workspace.

## Example prompts

- `فضای کاری فعال Maian من را بررسی کن.`
- `همه فاکتورهای تأییدشده را صفحه‌به‌صفحه بشمار و نام مشتری هرکدام را هم بیاور.`
- `برای این تیکت پاسخ عمومی ثبت کن و بعد از تأیید من نهایی‌اش کن.`
- `یک پیش‌نویس سند روزنامه متوازن با حساب‌های معتبر سیستم بساز و بعد از تأیید من ثبتش کن.`
- `برای کارهای تا سطح ریسک بالا تأیید همیشگی را فعال کن، ولی ارسال پیام یا اثر خارجی را شامل نکن.`
- `این پست بلاگ را برای فردا ساعت ۹ صبح منتشر کن.`

## Repository layout

- `.agents/plugins/marketplace.json` defines the installable marketplace.
- `plugins/maian-erp/.codex-plugin/plugin.json` defines plugin metadata.
- `plugins/maian-erp/.mcp.json` connects to the public Maian MCP endpoint.
- `plugins/maian-erp/skills/` contains reusable Codex workflow guidance.

## Security

This repository contains no user credentials or bearer tokens. Do not commit access tokens, refresh tokens, passwords, API keys, or private customer data. ERP permissions and tenant boundaries remain enforced by the Maian backend.

---

Maintained by [Maian](https://maian.app/).
