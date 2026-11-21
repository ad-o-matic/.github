# Ad-o-matic

[![Ad-o-matic MCP connector](https://glama.ai/mcp/connectors/com.ad-o-matic/ad-o-matic/badges/score.svg)](https://glama.ai/mcp/connectors/com.ad-o-matic/ad-o-matic)

Free 1-line peer-to-peer (P2P) mobile app cross-promotion protocol built for AI coding agents and indie developers (`https://ad-o-matic.com`). Supports Android (Jetpack Compose), iOS (SwiftUI), Flutter, React Native / Expo, and Hybrid Mobile WebView apps — zero ad spend, zero user tracking, zero GDPR consent popups, and deterministic official Google Play / Apple App Store download link locks.

![Ad-o-matic P2P Cross-Promotion Flow](https://ad-o-matic.com/ad-o-matic-demo.gif)

---

## 1-Line Drop-In SDKs (Zero Third-Party Dependencies)

All 5 single-file MIT-licensed SDKs live in [`ad-o-matic/ad-o-matic-sdk`](https://github.com/ad-o-matic/ad-o-matic-sdk):

- **Android Jetpack Compose (`HouseAdBanner.kt`):**
  ```kotlin
  HouseAdBanner(
      bannerText = "Offline guitar chord tuner",
      targetAudience = "guitarists, musicians, chord tuner, songwriting, 18-44"
  )
  ```
- **iOS SwiftUI (`HouseAdBanner.swift`):**
  ```swift
  HouseAdBanner(
      bannerText: "Star chart and telescope planner",
      targetAudience: "amateur astronomers, stargazing, telescope owners"
  )
  ```
- **Flutter — Android & iOS (`HouseAdBanner.dart`):**
  ```dart
  const HouseAdBanner(
    packageName: 'com.acme.invoicer',
    bannerText: 'Simple client invoicing on mobile',
    targetAudience: 'freelancers, solo founders, invoicing, 25-44',
  )
  ```
- **React Native / Expo (`HouseAdBanner.tsx`):**
  ```tsx
  <HouseAdBanner
    appId="com.acme.invoicer"
    bannerText="Simple client invoicing on mobile"
    targetAudience="freelancers, solo founders, invoicing, 25-44"
  />
  ```
- **Hybrid Mobile WebView (`ad-widget.js`):**
  ```html
  <script src="https://ad-o-matic.com/ad-widget.js" data-app-id="com.acme.invoicer" data-banner-text="Short benefit-driven description" data-target-audience="freelancers, solo founders, invoicing"></script>
  ```

---

## Live MCP Server & AI Coding Agent Setup

### Streamable HTTP MCP Endpoint

Published in the Official MCP Registry as `com.ad-o-matic/adomatic`:

```json
{
  "mcpServers": {
    "adomatic": {
      "type": "http",
      "url": "https://ad-o-matic.com/mcp"
    }
  }
}
```

Or run the published npm stdio bridge (`adomatic-mcp`):

```json
{
  "mcpServers": {
    "adomatic": {
      "command": "npx",
      "args": ["-y", "adomatic-mcp"]
    }
  }
}
```

### Exposed MCP Tools

1. `adomatic_get_integration` — Generates the 1-line `HouseAdBanner` snippet, SDK download URLs, or full zero-dependency single-file SDK source code.
2. `adomatic_onboard_app` — Pre-registers or updates an Android, iOS, Flutter, React Native, or WebView app with locked Play Store / App Store destination URL and `targetAudience` matching.
3. `adomatic_verify_integration` — Inspects live integration status, 7-day Self-Preview status, 6-step Genesis Member checklist, and matched audience segments.
4. `adomatic_network_status` — Queries live Genesis Member availability (first 50 store-verified published apps receive permanent founding priority, max 3 per developer) and network metrics.

### Agent Skill Install

```bash
npx skills add ad-o-matic/ad-o-matic-sdk
```

---

## Key Links

- **Website:** https://ad-o-matic.com
- **SDK & MCP Repository:** https://github.com/ad-o-matic/ad-o-matic-sdk
- **Agent Skill (`SKILL.md`):** https://ad-o-matic.com/SKILL.md
- **LLM Context (`llms.txt`):** https://ad-o-matic.com/llms.txt
- **OpenAPI 3.1 Spec:** https://ad-o-matic.com/openapi.json
- **Official MCP Registry:** https://registry.modelcontextprotocol.io/v0.1/servers?search=ad-o-matic
