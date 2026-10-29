# Smart Site Plan Map Data

Public GIS map data for any place in the United States, checked at the place and opened on a live map, right from your AI assistant.

Ask in plain words for utilities, parcels, zoning, flood zones or any other layer at a place. Smart Site Plan searches more than 20 million public GIS layers published by cities, counties, states, utilities and federal agencies, checks each candidate layer at your place, and answers with what it found and a link that opens your map with the data already on it.

This repository holds the public documentation, registry entry and Gemini CLI extension for Smart Site Plan's hosted MCP server. The server itself runs at Smart Site Plan; there is nothing to install.

## Connect

| | |
|---|---|
| Server URL | `https://api.smartsiteplan.com/mcp` |
| Transport | Streamable HTTP (remote) |
| Sign-in | None required; optional OAuth 2.1 with PKCE for a Smart Site Plan account |
| Registry name | `com.smartsiteplan/open-data` |

Add `https://api.smartsiteplan.com/mcp` as a custom connector in any assistant that supports remote MCP servers. Setup for each assistant: https://smartsiteplan.com/ai

It works without an account, with a little free usage each month. Signing in with a free Smart Site Plan account gives more, and saves each search as a conversation you can return to.

### Gemini CLI

```bash
gemini extensions install https://github.com/juno-maps/smart-site-plan-mcp
```

## Find data at a place

Ask for what you need and where, in one request. Each answer comes back within about 20 seconds. A longer search shows its progress and the map link, and your assistant follows it to the end.

When nothing public covers the request, it says so plainly. When the request is missing something, such as the place, it asks.

## Try

- "Show me sewer mains in Baltimore, MD"
- "Find water and sewer lines near 20425 Savin Hill Drive, Ashburn VA"
- "Flood zones in Wake County, NC"
- "Parcels over 1 acre near One Loudoun, Ashburn VA"
- "Zoning for downtown Austin, TX"

## Tools

| Tool | What it does | Changes data |
|---|---|---|
| `find_open_data` | Finds public map data at a place and returns the datasets and a map link | Saves the search as a conversation in your account |
| `check_open_data_search` | Follows a search that is still working until it ends | No |

## Permissions and privacy

The connector searches public open data only. It cannot read, change or delete your projects, layers, files or billing.

- It receives only your request text and, if you signed in, your account identity.
- Each search is stored as an Ask anything conversation under the same retention and privacy terms as any conversation in the app.
- Sign-in tokens last one hour, are bound to this server, and your consent is checked on every call.
- Disconnect any assistant at any time in Smart Site Plan under Account, Security, Connected AI assistants.

Privacy policy: https://smartsiteplan.com/privacy
Terms: https://smartsiteplan.com/terms
Security: https://smartsiteplan.com/security

## Learn more

- [Smart Site Plan for AI assistants](https://smartsiteplan.com/ai) (Markdown: [llms.txt](https://smartsiteplan.com/llms.txt))
- [Open data catalog](https://smartsiteplan.com/discover)

## Support

- Email: support@smartsiteplan.com
- Security reports: security@smartsiteplan.com (see [SECURITY.md](SECURITY.md))

Smart Site Plan is made by Juno Maps. The documentation in this repository is licensed under [CC BY 4.0](LICENSE).
