# Anytype MCP Server
[![smithery badge](https://smithery.ai/badge/@anyproto/anytype-mcp)](https://smithery.ai/server/@anyproto/anytype-mcp)

The Anytype MCP Server is a [Model Context Protocol (MCP)](https://modelcontextprotocol.io) server implementation, enabling AI assistants to seamlessly interact with [Anytype's API](https://github.com/anyproto/anytype-api) through natural language.

It bridges the gap between AI and Anytype's powerful features by converting Anytype's OpenAPI specification into MCP tools, allowing you to manage your knowledge base through conversation.

## Features

- Global & Space Search
- Spaces & Members
- Objects & Lists
- Properties & Tags
- Types & Templates

## Quick Start

### 1. Get Your API Key

1. Open Anytype
2. Go to Settings
3. Navigate to API Keys
4. Create a new API key

<details>
<summary>Alternative: Get API key via CLI</summary>

You can also get your API key using the command line:

```bash
npx -y @anyproto/anytype-mcp get-key
```

</details>

### 2. Configure Your MCP Client

Add the following configuration to your MCP client settings:

```json
{
  "mcpServers": {
    "anytype": {
      "command": "npx",
      "args": ["-y", "@anyproto/anytype-mcp"],
      "env": {
        "OPENAPI_MCP_HEADERS": "{\"Authorization\":\"Bearer <YOUR_API_KEY>\", \"Anytype-Version\":\"2025-05-20\"}"
      }
    }
  }
}
```

<details>
<summary>Alternative: Global Installation</summary>

If you prefer to install the package globally:

1. Install the package:

```bash
npm install -g @anyproto/anytype-mcp
```

2. Update your MCP client configuration to use the global installation:

```json
{
  "mcpServers": {
    "anytype": {
      "command": "anytype-mcp",
      "env": {
        "OPENAPI_MCP_HEADERS": "{\"Authorization\":\"Bearer <YOUR_API_KEY>\", \"Anytype-Version\":\"2025-05-20\"}"
      }
    }
  }
}
```

</details>

## Example Interactions

Here are some examples of how you can interact with your Anytype:

- "Create a new space called 'Project Ideas' with description 'A space for storing project ideas'"
- "Add a new object of type 'Task' with title 'Research AI trends' to the 'Project Ideas' space"
- "Create a second one with title 'Dive deep into LLMs' with due date in 3 days and assign it to me"
- "Now create a collection with the title "Tasks for this week" and add the two tasks to that list. Set due date of the first one to 10 days from now"

## Development

### Installation from Source

1. Clone the repository:

```bash
git clone https://github.com/anyproto/anytype-mcp.git
cd anytype-mcp
```

2. Install dependencies:

```bash
npm install -D
```

3. Build the project:

```bash
npm run build
```

4. Link the package globally (optional):

```bash
npm link
```

## Contribution

Thank you for your desire to develop Anytype together!

❤️ This project and everyone involved in it is governed by the [Code of Conduct](https://github.com/anyproto/.github/blob/main/docs/CODE_OF_CONDUCT.md).

🧑‍💻 Check out our [contributing guide](https://github.com/anyproto/.github/blob/main/docs/CONTRIBUTING.md) to learn about asking questions, creating issues, or submitting pull requests.

🫢 For security findings, please email [security@anytype.io](mailto:security@anytype.io) and refer to our [security guide](https://github.com/anyproto/.github/blob/main/docs/SECURITY.md) for more information.

🤝 Follow us on [Github](https://github.com/anyproto) and join the [Contributors Community](https://github.com/orgs/anyproto/discussions).

---

Made by Any — a Swiss association 🇨🇭

Licensed under [MIT](./LICENSE.md).
