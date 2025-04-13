# VS Code Config

### Files tracked

- settings.json
- extensions.txt

## Notes/Examples

- `commands.json` + `terminals.json`

```json
{
  "commands": [
    {
      "command": "commands.refresh",
      "text": "$(sync)",
      "tooltip": "Refresh commands",
      "color": "#FFCC00"
    },
    {
      "text": "$(terminal)",
      "color": "#00FF00",
      "command": "terminals.runTerminalByName",
      "arguments": ["activateVenv"],
      "tooltip": "activate venv"
    },
    {
      "text": "$(terminal)",
      "color": "#FF0000",
      "command": "terminals.runTerminalByName",
      "arguments": ["deactivateVenv"],
      "tooltip": "deactivate venv"
    }
  ]
}
```

```json
{
  "terminals": [
    {
      // default terminal
      "name": "activateVenv",
      "icon": "code",
      "color": "terminal.ansiGreen",
      "cwd": "/Users/julio-gonzalez/oil-and-gas",
      "shell": "cmd.exe",
      "open": true,
      "focus": true,
      "commands": ["clear", "venv\\Scripts\\activate"]
    },
    {
      "name": "deactivateVenv",
      "target": "activateVenv",
      "commands": ["clear", "deactivate"]
    }
  ]
}
```
