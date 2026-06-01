## Andy Worford

I build agentic systems that run ops workflows end-to-end. No human in the loop for the routine stuff.

Current project: **A(I)DEN**, an autonomous vendor operations platform built on Anthropic's Claude Agent SDK and Claude Code. It handles the full vendor lifecycle for a lead-gen marketplace: inbox triage, vendor briefs, contract routing, monday.com mutations, Phonexa campaign config, disposition ingests, and billing reconciliation. Ships to production daily.

**What's under the hood:**

- 370+ Node.js modules orchestrated by Claude Code as the runtime shell
- Multi-agent dispatch: Claude Sonnet subagents fire in parallel for independent workstreams; Opus holds front-of-house context
- 424 machine-readable SOP rule files loaded as structured context. The system "knows" vendor policy the way a trained employee would
- MCP server integrations: Gmail, Google Calendar, Drive, monday.com, Airtable, Jira
- Voice calibration: Andy-voice model trained on 4,089 historical sent emails so outbound drafts match the owner's register
- CDP automation via Chromium for authenticated scrapes (Phonexa reports, Gmail snooze, Box Sign status)
- Bidirectional Drive sync across 3 machines with fork-safety rules

**Stack:** Node.js · Anthropic Claude API · MCP (Model Context Protocol) · Gmail API · monday.com GraphQL · Google Workspace OAuth · Puppeteer/CDP · PostgreSQL

**Background:** Vendor ops + lead-gen marketplace (solar, roofing, windows, bathroom). Previously built lead routing and affiliate tracking tooling. Now all of it runs on agentic infrastructure.

Most of the production code is private. Public architecture overview at **[aiden-overview](https://github.com/andy-bttryzn/aiden-overview)**. Happy to walk through more in conversation.

---

### Public portfolio

The patterns and tooling that survived A(I)DEN's daily production grind, extracted as standalone projects:

| | |
|---|---|
| 🏛️ **[aiden-overview](https://github.com/andy-bttryzn/aiden-overview)** | The architectural cross-section. Three operational lanes, multi-agent dispatch, SOP corpus, voice calibration, CDP automation, Drive sync. |
| 📘 **[vendor-ops-playbook](https://github.com/andy-bttryzn/vendor-ops-playbook)** | 14-chapter operating manual for running vendor-heavy operations. Read [chapter 1](https://github.com/andy-bttryzn/vendor-ops-playbook/blob/main/chapters/01-the-vendor-ops-model.md) for the mental model, [chapter 12](https://github.com/andy-bttryzn/vendor-ops-playbook/blob/main/chapters/12-30-day-adoption-guide.md) for a week-by-week adoption plan. |
| 🧰 **[vendor-brief-renderer](https://github.com/andy-bttryzn/vendor-brief-renderer)** | Structured `vendor.json` in, 10-section Markdown brief out. Includes a CSV adapter showing the data-source boundary. |
| ✉️ **[gworkspace-helper](https://github.com/andy-bttryzn/gworkspace-helper)** | Google Workspace CLI with opinionated draft validation. The reason no LLM-toned cold opens reach the customers. |
| 🗂️ **[monday-helper](https://github.com/andy-bttryzn/monday-helper)** | monday.com CLI + Node library. Auth, reads, writes, opt-in dedup. |
| 📚 **[docs-mirror-scraper](https://github.com/andy-bttryzn/docs-mirror-scraper)** | Pull any docs site into a local Markdown mirror for offline / LLM-context use. |

79 tests across the four code repos, CI on Node 18/20/22/24, MIT across the board.

---

[LinkedIn](https://www.linkedin.com/in/andy-worford/) · [Email](mailto:andy@bttryzn.com)
