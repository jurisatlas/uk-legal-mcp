# United Kingdom Legal Research MCP Server (`uk-legal-mcp`)

## English Documentation

Model Context Protocol (MCP) server providing live, read-only access to **United Kingdom (UK)** legislation, official gazettes, multi-tier judicial decisions (First Instance, Regional/Cantonal/Appellate, and Supreme/Constitutional courts, including HTML and PDF full-text extraction), and statutory citation verification across all major AI clients (**ChatGPT Desktop, OpenAI Codex CLI, Claude Desktop, Claude Code CLI, Cursor, Windsurf, VS Code / GitHub Copilot / Cline / Roo Code, Google Antigravity / Gemini CLI, Perplexity, and Continue.dev**).

---

### Interactive Desktop Setup (Select Your AI Assistant)

This package includes a graphical installer for legal practitioners and non-technical users that lets you select which AI application(s) you use:

1. **Download:** Click **`<> Code`** at the top right of this repository, select **`Download ZIP`**, and extract the folder to your computer.
2. **Run the Setup Utility:**
   - **Windows:** Double-click `Click_Here_To_Install_Windows.bat`
   - **macOS:** Double-click `Click_Here_To_Install_Mac.command`
3. **Select Your AI Client(s) & Connect:** Check the box(es) for the AI assistant(s) installed on your computer (**ChatGPT Desktop & OpenAI Codex CLI**, **Claude Desktop & Claude Code CLI**, **Cursor**, **Windsurf**, **VS Code / GitHub Copilot / Cline / Roo Code**, **Google Antigravity / Gemini CLI**, or **Perplexity / Continue.dev**), click **Install to Selected AI Clients**, and restart your selected AI application.

**System Integrity Note:** The setup utility operates strictly in read-only mode with respect to your personal files and documents. It installs an isolated Python runtime inside the extracted folder and registers the server entry only in the AI client configuration files you select.

---

### Multi-Tier Judicial Hierarchy & Live Indexed National Archives

This server performs live queries across the full judicial hierarchy and official legal archives of **United Kingdom**, extracting full text from both HTML pages and official court/gazette PDF judgments:

| Judicial Tier | Covered Courts & Tribunals |
|:---|:---|
| **Tier 1 — First Instance** | County Court, Crown Court, High Court of Justice (EWHC — King's Bench, Chancery, Family, Commercial, Administrative) & First-tier Tribunals (FTT) |
| **Tier 2 — Regional / Cantonal / Appellate** | Court of Appeal of England & Wales (EWCA Civil & Criminal Divisions), Inner House of the Court of Session (Scotland), Court of Appeal in Northern Ireland & Upper Tribunals (UKUT / EAT) |
| **Tier 3 — Supreme & Constitutional** | United Kingdom Supreme Court (UKSC) & Judicial Committee of the Privy Council (JCPC) |

#### Official Portals & Live Indexed Domains

- **National Legislation & Official Gazette:** UK Legislation API (legislation.gov.uk) & i.AI Lex API (lex.lab.i.ai.gov.uk) — [https://www.legislation.gov.uk](https://www.legislation.gov.uk)
  - *Indexed Legislation Domains:* `legislation.gov.uk`
- **Court Decisions & Jurisprudence Archives:** The National Archives Find Case Law (caselaw.nationalarchives.gov.uk) & BAILII — [https://caselaw.nationalarchives.gov.uk](https://caselaw.nationalarchives.gov.uk)
  - *Indexed Judicial & Open Case Law Domains:* `caselaw.nationalarchives.gov.uk`, `judiciary.uk`, `bailii.org`, `supremecourt.uk`

---

### Available MCP Tools

| Tool | Description |
|:---|:---|
| `search_legislation` | Searches enacted statutes, codes, decrees, and official gazette publications in United Kingdom. |
| `search_case_law` | Searches national jurisprudence and open judicial archives for United Kingdom. |
| `search_tiered_court_decisions` | Filters case law specifically by judicial instance (`first_instance`, `appellate_regional`, `supreme_constitutional`) or specific regional/cantonal/district court. |
| `list_court_hierarchy` | Returns the complete 3-tier court structure and supported regional court filters for United Kingdom. |
| `get_legal_document_markdown` | Retrieves full statutory or judicial texts (both HTML and official `.pdf` court judgments) and converts them into clean Markdown. |
| `verify_citation` | Validates statutory and case law citations against official registries. |

---

<details>
<summary><b>Manual Configuration for Developers (Optional)</b></summary>

```json
{
  "mcpServers": {
    "uk-legal-mcp": {
      "command": "uvx",
      "args": [
        "--from",
        "https://github.com/jurisatlas/uk-legal-mcp/archive/refs/heads/main.zip",
        "uk-legal-mcp"
      ]
    }
  }
}
```
</details>
