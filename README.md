# Tako MCP
Tako MCP is a simple MCP server that queries Tako and returns real-time data and visualization

Check out [Tako](https://trytako.com) and our [documentation](https://docs.trytako.com)


## Quickstart
###  Get your API key
Access [Tako Dashboard](https://trytako.com/dashboard) and get your API key. 

### Add Tako MCP to Claude Desktop
Add the following to your `.cursor/mcp.json` or `claude_desktop_config.json` (MacOS: `~/Library/Application\ Support/Claude/claude_desktop_config.json`)
```json Python
{
    "mcpServers": {
        "takoApi": {
            "command": "uv",
            "args": [
                "--directory",
                "/path/to/tako/mcp",
                "run",
                "main.py"
            ],
            "env": {
                "TAKO_API_KEY": "<TAKO_API_KEY>"
            }
        }
    }
}
```

## Example:
### 1. Use the prompt from Tako MCP Server `generate_search_tako_prompt`
The prompt will guide the model to generate optimized query to search Tako
### 2. Add your text input 
Add an input text to generate the prompt
> "Compare Magnificent 7 stock companies on relevant metrics."
### 3. Add a prompt to the chat 
Add additional instructions to the chat prompt
> Write me a research report on the magnificent 7 companies. Embed the result in an iframe whenever necessary
### 4. Checkout the result
  * [Claude Response](https://claude.ai/share/0c39e0c3-0811-486e-8f0b-92c8d5e05bc8)
  * [Generated Report](https://docs.trytako.com/documentation/integrations-and-examples/claude-generated-report)