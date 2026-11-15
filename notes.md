# Notes for the Agentic Coding workshop.

## Using GitHub. 
- `git config --global user.name "GitHub username"` configures your Git username.
- `git config --global user.email "GitHub email"` configures your Git email.

### Basic terminal commands for Git.
- `git init` initializes an empty repository inside whatever directory you are.
- `git add ` adds whatever files are being specified into the git repository.
- `git status` shows you the status of your Git repository, shows you what files have been changed, what files have been added and what has to be done. 
- `git commit -m "Commit Message"` commits a change to your Git repository.
- `git push -u origin main` pushes you commit to the Git repository.
- `git log` shows you everything you've done in the repository so far, the commits and the changes.

### Connecting Penpot to Antigravity (MCP Setup)

#### 1. Generate Penpot MCP Token
1. Open Penpot → click **Profile icon** → **Your account** → **Integrations**.
2. Toggle **MCP Server** to **Enabled** and generate your token.
3. Copy the token.

#### 2. Configure Antigravity (`mcp_config.json`)
1. Open the **Agent** panel on the right (`Ctrl+L` or `Ctrl+Shift+I`), click **`...`** → **MCP Servers** → **Manage MCP Servers** → **View raw config**.
2. Add the Penpot endpoint using `"serverUrl"` (not `"url"`):

```json
{
  "mcpServers": {
    "penpot": {
      "serverUrl": "[https://design.penpot.app/mcp/stream?userToken=yourmcpkey:)](https://design.penpot.app/mcp/stream?userToken=yourmcpkey:))"
    }
  }
}