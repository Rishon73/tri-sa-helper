# tri-sa-helper

> Tri-make-life-easier: A growing collection of PowerShell functions that make daily demo environment ops slightly less painful. You're welcome.

---

## Installation

1. Download `Microsoft.PowerShell_profile.ps1` from this repo
2. Drop it into:
   ```
   C:\Users\<YOUR_TRI_SHORT_USER_NAME>\OneDrive - TRICENTIS\Documents\WindowsPowerShell\
   ```
3. Open a new PowerShell window — the functions load automatically on startup

> **Note:** If a `Microsoft.PowerShell_profile.ps1` already exists in that folder, merge the functions manually rather than overwriting.

---

## Usage

To see all available functions at any time, run:

```powershell
Tri-show
```

---

## Available Functions

| Function | Description |
|---|---|
| `Tri-show` | Lists all available helper functions and the current version |
| `Tri-get-version` | Returns the current script version |
| `Tri-env-start` | Full environment startup sequence (license config, OSV, DEX agent, TriServe) |
| `Tri-launch-Tosca` | Clears the Tosca lock file (if needed) and launches Tosca Commander |
| `Tri-launch-Tosca-license-configuration` | Opens the Tosca License Configuration tool |
| `Tri-delete-Tosca-lock-file [-force]` | Deletes the Tosca workspace lock file; prompts for confirmation if Tosca is running, `-force` skips the prompt |
| `Tri-Start-OSVEnvironment` | Starts the OSV environment via the local API |
| `Tri-launch-LocalDEXAgent` | Launches the Tosca Distribution (DEX) Agent |
| `Tri-launch-TriServeWebMonitor` | Starts the TriServe Web Monitor; auto-detects the correct path based on hostname |
| `Tri-launch-vision-ai-agent` | Launches the Vision AI Agent |
| `Tri-launch-di-report-viewer` | Opens the Data Integrity Report Viewer |
| `Tri-launch-E2G-agent [-personalAgent] [-liveView]` | Launches the E2G agent; defaults to shared mode for the `amspresales` tenant |
| `Tri-launch-sim-agent` | Launches the Tricentis Simulator Agent from the Downloads folder |
| `Tri-launch-dotNet-OrderView` | Launches OrderView; starts TriServe Web Monitor first if it's not already running |
| `tri-launch-dex-mcp [-port <int>]` | Launches the TBox MCP server in a new PowerShell window; defaults to port 5000 |

---

## Requirements

- Windows PowerShell 5.1 or PowerShell 7+
- Tricentis Tosca installed on the machine
- Relevant environment variables set (e.g., `TRICENTIS_HOME`, `TRICENTIS_DEX_AGENT_HOME`, `TRICENTIS_DI_HOME`)

---

## Contributing

Got a function that saves you five clicks a day? Add it, commit it, push it. That's the spirit.
