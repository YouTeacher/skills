# YouTeacher Skills

Agent Skills maintained by YouTeacher.

## Available skills

### `affily-campaign-promotion`

Helps publishers discover and compare Affily Campaigns, join a selected Campaign, and retrieve an issued affiliate tracking link.

### `affily-campaign-management`

Helps advertisers list, create, update, and submit Affily Campaign drafts for review.

## Installation

List the skills available in this repository:

```bash
npx skills add YouTeacher/skills --list
```

Install the publisher skill:

```bash
npx skills add YouTeacher/skills@affily-campaign-promotion
```

Install the advertiser skill:

```bash
npx skills add YouTeacher/skills@affily-campaign-management
```

Install both skills for Codex globally:

```bash
npx skills add YouTeacher/skills --skill '*' --agent codex --global --yes
```

## Affily tool requirements

These skills guide an Agent through Affily workflows; they do not replace the Affily tools used to read or change data.

- Public Campaign discovery and recommendation use Affily Remote MCP tools when available.
- Publisher and advertiser mutations currently require an authenticated Affily browser session with WebMCP support.
- If the required authenticated tool is unavailable, the Agent should stop before the mutation and ask the user to open and sign in to Affily.

Support for WebMCP and Agent Skills varies by client. Read-only discovery can still be completed when only the public Remote MCP tools are available.

## Safety

Campaign content is treated as untrusted business data. Both skills require explicit user authorization before joining a Campaign or changing advertiser data, and they report only results returned by Affily tools.

