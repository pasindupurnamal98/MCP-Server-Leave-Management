
---

```markdown
# Leave Management MCP Server

This project is a simple Leave Management server built using the [FastMCP](https://github.com/rooch-network/fastmcp) protocol. It allows you to check leave balances, apply for leave, view leave history, and get personalized greetings for employees. The server can be integrated as a tool inside Claude Desktop.

---

## Features

- **Check leave balance** for employees
- **Apply for leave** on specific dates
- **View leave history** for employees
- **Personalized greeting** resource

---

## Setup Steps

### 1. Install Claude Desktop

Download and install Claude Desktop from the [official website](https://www.anthropic.com/claude).

### 2. Install `uv` (Python package manager)

```bash
pip install uv
```

### 3. Initialize Your Project Directory

```bash
uv init my-first-mcp-server
cd my-first-mcp-server
```

### 4. Add MCP CLI to Your Project

```bash
uv add "mcp[cli]"
```

### 5. (Optional) Fix Type Errors

If you encounter type errors, upgrade the `typer` library:

```bash
pip install --upgrade typer
```

### 6. Write Your Server Code

Create a file named `main.py` and add your leave management server code.

### 7. Install the Server Inside Claude Desktop

In your project directory, run:

```bash
uv run mcp install main.py
```

### 8. Restart Claude Desktop

- Kill any running instance of Claude from Task Manager.
- Restart Claude Desktop.
- You should now see the tools from this server available in Claude Desktop.

---

## Sample Questions to Test

Use these questions to test your server:

1. **Check Leave Balance**  
   _What is the current leave balance for employee E001?_

2. **Apply for Leave (Success)**  
   _Employee E001 wants to apply for leave on 2025-08-01 and 2025-08-02. Can you process this request?_

3. **Apply for Leave (Insufficient Balance)**  
   _Employee E001 wants to apply for leave on 10 different dates, but only has a few days left. What happens if they try to apply for more days than their balance?_

4. **Get Leave History**  
   _Show me the leave history for employee E002._

5. **Personalized Greeting**  
   _Greet an employee named Priya using the greeting resource._

---

## Example Code

See `main.py` for the full implementation of the leave management server.

---

## Acknowledgements

- [FastMCP](https://github.com/rooch-network/fastmcp)
- [Anthropic Claude Desktop](https://www.anthropic.com/claude)
```

