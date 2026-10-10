# Google Search Console MCP Server by Insightful Pipe

[![MCP Compatible](https://img.shields.io/badge/MCP-Compatible-blue)](https://insightfulpipe.com/mcp-servers/google-search-console)
[![Insightful Pipe](https://img.shields.io/badge/Insightful_Pipe-MCP_Servers-purple)](https://insightfulpipe.com/mcp-servers)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> **Connect Google Search Console to AI assistants for SEO analytics and search performance insights.**

Part of the [Insightful Pipe MCP Server Collection](https://insightfulpipe.com/mcp-servers) — The Google Search Console MCP server enables Claude, ChatGPT, Cursor, and other AI assistants to analyze your website's search performance. Monitor rankings, track clicks, and get AI-powered SEO recommendations.

[![Explore All MCP Servers](https://img.shields.io/badge/Explore_All-MCP_Servers-blue?style=for-the-badge)](https://insightfulpipe.com/mcp-servers)

![Google Search Console MCP Server](https://insightfulpipe.com/images/google-search-console-icon.svg)

## MCP Server URL

```
https://google-search-console.insightfulmcp.com/
```

## What is Google Search Console MCP?

Google Search Console MCP is a **remote Model Context Protocol server** that provides AI assistants with access to your GSC data. This SEO-focused integration allows you to:

- Query search performance using natural language
- Analyze keyword rankings and click-through rates
- Identify indexing issues and coverage problems
- Get AI-powered SEO recommendations
- Inspect individual URLs for indexing status

## Installation

### Claude

1. Copy the MCP Server URL: `https://google-search-console.insightfulmcp.com/`
2. Open [Claude Connectors Settings](https://claude.ai/settings/connectors)
3. Scroll to the bottom and click **Add custom connector**
4. Paste the URL and click **Add**
5. Click **Connect** and sign in to InsightfulPipe if asked. Claude then lists the connector as connected.

### ChatGPT

Custom MCP servers are added through ChatGPT's **Developer mode**. Availability depends on your ChatGPT plan, and workspace admins may need to allow it.

1. Turn on **Developer mode** in ChatGPT settings
2. Create a new app for a remote MCP server and paste the URL: `https://google-search-console.insightfulmcp.com/`
3. Sign in to InsightfulPipe if asked. The connection finishes as soon as you are signed in.

See OpenAI's guide: [Developer mode and MCP apps in ChatGPT](https://help.openai.com/en/articles/12584461-developer-mode-and-mcp-apps-in-chatgpt)

### Claude Code

```bash
claude mcp add --transport http google-search-console https://google-search-console.insightfulmcp.com/
```

### Cursor

Add the server to `~/.cursor/mcp.json` (all projects) or `.cursor/mcp.json` (one project):

```json
{
  "mcpServers": {
    "google-search-console": {
      "url": "https://google-search-console.insightfulmcp.com/"
    }
  }
}
```

When Cursor shows **Needs authentication**, click **Connect** and sign in to InsightfulPipe if asked.

## Available Actions

10 actions: 8 read, 2 write.

### Read Actions (8)

| Action | Description |
|--------|-------------|
| `batch_url_inspection` | Inspect multiple URLs in one call for indexing status, mobile usability, and rich results (max 50) |
| `check_indexing_issues` | Audit top pages by traffic for indexing issues, canonical mismatches, and mobile problems |
| `search_analytics` | Search performance data including clicks, impressions, CTR, and position grouped by dimensions |
| `site_info` | Get information for a specific Search Console property |
| `sitemap_info` | Get detailed information for a specific sitemap |
| `sitemaps_list` | List all sitemaps submitted for a property |
| `sites_list` | List all Search Console properties accessible to the account |
| `url_inspection` | Inspect indexing status, mobile usability, and rich results for a URL |

### Write Actions (2)

| Action | Description |
|--------|-------------|
| `delete_sitemap` | Remove a submitted sitemap from Google Search Console |
| `submit_sitemap` | Submit a new sitemap to Google Search Console for a property |

## Control What Your AI Can Do

You decide what AI agents can do with each connected account:

- **Turn individual actions on or off** for every connected account, so agents only see the actions you allow.
- **Connect as Read-only or Read & Write.** A read-only connection can only enable read actions.
- **Destructive actions stay off by default.** Actions such as deletes are disabled until an admin enables them.
- **Team access per account.** Restricted team members only use the accounts they are granted, with the read actions enabled on them.

## Usage Examples

### Search Performance Overview

```
"How is my site performing in Google Search this month?"
```

### Keyword Analysis

```
"What are my top 20 keywords by clicks?"
```

### Ranking Opportunities

```
"Which keywords am I ranking on page 2 that have high impressions?"
```

### CTR Optimization

```
"Which pages have low CTR but high impressions?"
```

### URL Inspection

```
"Check the indexing status of https://mysite.com/new-page"
```

### Sitemap Status

```
"Show me the status of my submitted sitemaps"
```

## Supported Metrics

| Metric | Description |
|--------|-------------|
| Clicks | Total clicks from search |
| Impressions | Times shown in search results |
| CTR | Click-through rate |
| Average Position | Average ranking position |

## Why Google Search Console MCP?

### For SEO Professionals
- **Faster analysis** - Query data conversationally
- **Opportunity discovery** - AI finds ranking opportunities
- **Technical auditing** - Identify indexing issues quickly

### For Content Marketers
- **Content performance** - See which content ranks
- **Keyword research** - Discover what you rank for
- **Optimization priorities** - Know what to improve first

### For Website Owners
- **Search visibility** - Understand Google Search presence
- **Problem detection** - Catch issues early
- **Growth tracking** - Monitor SEO progress

## SEO Workflow Examples

### Find Quick Wins

```
"Show me keywords ranking between position 8-20 with more than 100 impressions"
```

### Content Audit

```
"Which of my blog posts are getting the most clicks from search?"
```

### Technical Health Check

```
"Inspect the indexing status of my homepage"
```

## Security & Privacy

- **Official Search Console API** - Direct integration with Google's API
- **OAuth 2.0** - Secure Google authentication
- **Data encryption** - Secure transmission

## Pricing

The Google Search Console MCP server is included in every InsightfulPipe plan, together with all other MCP servers and the CLI. Plans start at $29.99/month, and you can try it for 7 days. See [insightfulpipe.com/pricing](https://insightfulpipe.com/pricing) for current plans.

## Ready-Made Skills and Prompts

- [Claude skills for SEO and marketing](https://insightfulpipe.com/marketing-claude-skills/marketing) — ready-made skills that run on your connected data
- [Search Console Performance Overview](https://insightfulpipe.com/marketing-prompts-library/google-search-console-search-console-performance-overview)
- [Keyword Ranking Analysis](https://insightfulpipe.com/marketing-prompts-library/google-search-console-keyword-ranking-analysis)
- [Search Console Indexing Status Check](https://insightfulpipe.com/marketing-prompts-library/google-search-console-search-console-indexing-status-check)

## Explore More MCP Servers by Insightful Pipe

Visit **[insightfulpipe.com/mcp-servers](https://insightfulpipe.com/mcp-servers)** to discover our full collection of MCP servers for marketing and analytics.

### SEO & Performance MCP Servers
- [Google Analytics MCP](https://insightfulpipe.com/mcp-servers/google-analytics) - Website analytics
- [PageSpeed MCP](https://insightfulpipe.com/mcp-servers/pagespeed) - Performance metrics
- [Web Crawler MCP](https://insightfulpipe.com/mcp-servers/crawler) - Site crawling
- [Google My Business MCP](https://insightfulpipe.com/mcp-servers/google-my-business) - Local SEO

### Advertising MCP Servers
- [Google Ads MCP](https://insightfulpipe.com/mcp-servers/google-ads) - Google advertising
- [Facebook Ads MCP](https://insightfulpipe.com/mcp-servers/facebook-ads) - Meta advertising

**[View All MCP Servers →](https://insightfulpipe.com/mcp-servers)**

## Resources

- [Documentation](https://insightfulpipe.com/docs/connectors-google-search-console)
- [Video Tutorial](https://www.youtube.com/playlist?list=PLJNzvjxzI5Xwe__BJJLAelSF0ewO3mEFk)
- [InsightfulPipe Blog](https://insightfulpipe.com/blog)

## Support

- **Documentation**: [insightfulpipe.com/docs](https://insightfulpipe.com/docs)
- **All MCP Servers**: [insightfulpipe.com/mcp-servers](https://insightfulpipe.com/mcp-servers)
- **Email**: support@insightfulpipe.com

---

**[Insightful Pipe](https://insightfulpipe.com)** — AI-powered marketing analytics through MCP servers. [Explore all integrations →](https://insightfulpipe.com/mcp-servers)

## License

MIT License - see [LICENSE](LICENSE) for details.
