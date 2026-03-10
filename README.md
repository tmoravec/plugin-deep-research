## Deep Research

Perform deep research on a specific topic and compile a final report with the ability to draft a research plan, search the web, and read web pages.

This plugin uses **Brave Search** (via n8n webhook) and a **Plugin Server** for reading web pages. You need to provide an n8n token and a Plugin Server URL to start using it.

### Setup

1. **n8n Token**: Token for authenticating the n8n webhook that triggers the Brave Search workflow.
2. **Plugin Server URL**: The URL of your Plugin Server instance used to read web page content. [Learn how to deploy a Plugin Server](https://docs.typingmind.com/plugins/plugins-server/how-to-deploy-plugins-server-on-render).

### Research Mode

- **Lightweight Mode**: Deep Research uses search result snippets from Brave Search to gather information. Web pages are only read when snippets don't contain enough detail. This is the default mode.
- **Comprehensive Mode**: Deep Research reads the full content of each relevant web page to ensure the most accurate and complete answer. This consumes more tokens and may take longer.

### Customizable
The Deep Research plugin is customizable. You can duplicate this plugin and add your own tools to enhance the quality of the final report. The system instructions and prompts are also available in the plugin source.

By default, the Deep Research plugin comes with 3 tools: Research Plan, Search Web, and Read Web Page. Depending on your specific needs, you can add more tools like reading from a tweet, searching from a private database, or controlling a browser. The TypingMind plugin system allows you to add multiple tools to the Deep Research plugin and supports various ways to implement your tools using JavaScript, HTTP requests, or MCP.

[Learn how to develop TypingMind plugins here](https://www.typingmind.com/plugins-docs).

## Token Usage
This plugin may use multiple tools in multiple turns. A deep research task can run for up to 2 minutes. Please monitor the token usage closely to avoid consuming too many tokens. You can also modify the plugin to make it more token-efficient by adding your own tools to perform web searches and read web pages.

### Example Usage

> Compare the current latest EV cars and their prices available for purchase in the EU.
