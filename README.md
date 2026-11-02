# Oceanir MCP and assistant connectors

Official distribution metadata for Oceanir's hosted MCP server: **https://mcp.oceanir.ai**.

Oceanir investigates where an image may have been taken and assesses consistency with a claimed location. It returns candidate places, visual clues and uncertainty. It does not identify people, track people, establish capture dates or guarantee an exact address.

## Connect

Use your assistant's remote MCP/custom connector setup and enter `https://mcp.oceanir.ai`. Sign in to Oceanir through OAuth. For Claude Code:

```sh
claude mcp add --transport http oceanir https://mcp.oceanir.ai
```

Tools: `geolocate_image`, `verify_location_claim`, `check_credits`. Analysis calls use your Oceanir credits and require eligible access; tool discovery is public. Check [pricing](https://oceanir.ai/pricing) before running analyses. Share only images you are authorized to submit.

- [Documentation](https://oceanir.ai/docs/mcp)
- [Privacy](https://oceanir.ai/privacy)
- [Terms](https://oceanir.ai/terms)
- [Support](https://oceanir.ai/contact)

## Distribution files

`server.json` describes the hosted server under `io.github.Oceanir/oceanir`. `plugin/` contains the portable assistant plugin package. A manifest in this repository is not evidence that every store has approved the connector.

The GitHub Actions workflow publishes registry metadata using short-lived GitHub OIDC identity. It does not publish model code, use an npm package, store a GitHub PAT, or deploy the Oceanir application. Only organization maintainers should dispatch it, from the main branch. Registry versions are immutable; increment the version for later publications.

Package metadata and local distribution files are MIT licensed. Hosted Oceanir access remains governed by its service terms.
