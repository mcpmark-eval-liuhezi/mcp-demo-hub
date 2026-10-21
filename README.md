# mcp-demo-hub
Demo showcase: an agent driving GitHub end-to-end, with live-researched upstream notes on the official GitHub MCP Server.

## Upstream notes

Upstream repository: **github/github-mcp-server** — "GitHub's official MCP Server" (primary language: Go; 33,829 stars at time of writing).

Two most recently updated merged pull requests upstream, summarized from their diffs:

- **#3540 — "upgrade to Go 1.27.3 for compromised CA mitigation"**: bumps the Go toolchain to 1.27.3 across go.mod, the Docker builder image, CI workflows, and contributor docs (plus mechanical Go 1.27 code modernizations) so rebuilt binaries reject the compromised eMudhra certificate chains.
- **#1652 — "Add aliases for new actions tools"**: maps 16 older workflow/actions tool names to their consolidated replacements (`actions_list`, `actions_get`, `actions_run_trigger`) in `deprecated_tool_aliases.go` and the tool-renaming docs, so existing MCP server configurations keep working after the tool consolidation.
