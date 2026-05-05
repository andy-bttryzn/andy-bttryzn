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

Most of the production code is private. Happy to walk through architecture in conversation.

---

[LinkedIn](https://www.linkedin.com/in/andy-worford/) · [Email](mailto:andy@bttryzn.com)
