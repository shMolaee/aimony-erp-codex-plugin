# AIMony ERP for Codex

AIMony ERP connects Codex to an authenticated AIMony workspace for workspace-aware reporting and governed ERP actions.

## Direct download

- [Download AIMony ERP for Codex v0.1.0](https://app.aimony.ir/downloads/standalone/codex/aimony-erp/aimony-erp-codex-plugin-v0.1.0.zip)
- [Download the latest package](https://app.aimony.ir/downloads/standalone/codex/aimony-erp/aimony-erp-codex-plugin.zip)
- [SHA-256 checksum](https://app.aimony.ir/downloads/standalone/codex/aimony-erp/aimony-erp-codex-plugin-v0.1.0.zip.sha256)

After downloading, extract the ZIP and add its root directory as a local Codex marketplace:

```powershell
codex plugin marketplace add C:\path\to\aimony-erp-codex-plugin-v0.1.0
codex plugin add aimony-erp@aimony-erp
```

## Capabilities

- Inspect the active workspace.
- List and count customers, products, tickets, and invoices with pagination and filters respected.
- Create governed ERP proposals and finalize the exact proposal after explicit confirmation.
- Create or update blog posts, using draft status by default and publishing only when explicitly requested.
- Guide sign-in through Codex without exposing OAuth, token, or command-line details to end users.

## Install from GitHub

Add this repository as a Codex plugin marketplace:

```powershell
codex plugin marketplace add shMolaee/aimony-erp-codex-plugin
```

Then install the plugin:

```powershell
codex plugin add aimony-erp@aimony-erp
```

Open a new Codex task after installation. On first use, Codex starts the AIMony sign-in flow. Each user authenticates against their own AIMony account and workspace.

## Example prompts

- `فضای کاری فعال AIMony من را بررسی کن.`
- `چند مشتری و چند فاکتور در این workspace داریم؟`
- `یک پیش‌نویس پست بلاگ برای معرفی محصول جدید بساز.`
- `این عملیات را پیشنهاد بده و بعد از تأیید من نهایی کن.`

## Repository layout

- `.agents/plugins/marketplace.json` defines the installable marketplace.
- `plugins/aimony-erp/.codex-plugin/plugin.json` defines the plugin metadata.
- `plugins/aimony-erp/.mcp.json` connects to the public AIMony MCP endpoint.
- `plugins/aimony-erp/skills/` contains the reusable Codex workflow guidance.

## Security

This repository contains no user credentials or bearer tokens. Do not commit access tokens, refresh tokens, passwords, API keys, or private customer data. ERP permissions and tenant boundaries remain enforced by the AIMony backend.

---

Maintained by [Aimori](https://aimony.ir/).
