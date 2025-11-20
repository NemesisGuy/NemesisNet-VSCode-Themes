# Installation & Setup Guide

## Quick Installation (Manual)

Since this theme is custom-built for your brand, here's how to install it manually:

### Step 1: Locate Your VSCode Extensions Folder

**Windows:**
```
%USERPROFILE%\.vscode\extensions\
```
Full path example: `C:\Users\YourUsername\.vscode\extensions\`

**macOS:**
```
~/.vscode/extensions/
```
Full path example: `/Users/YourUsername/.vscode/extensions/`

**Linux:**
```
~/.vscode/extensions/
```
Full path example: `/home/YourUsername/.vscode/extensions/`

### Step 2: Copy the Theme Folder

1. Copy the entire `NemesisNet-VSCode-Theme` folder
2. Paste it into your VSCode extensions folder
3. The final path should look like:
   - Windows: `C:\Users\YourUsername\.vscode\extensions\NemesisNet-VSCode-Theme\`
   - macOS/Linux: `~/.vscode/extensions/NemesisNet-VSCode-Theme/`

### Step 3: Activate the Theme

1. **Restart VSCode** (or reload window with `Ctrl+R` / `Cmd+R`)
2. Press `Ctrl+K Ctrl+T` (or `Cmd+K Cmd+T` on macOS) to open the theme picker
3. Select one of the NemesisNet themes:
   - NemesisNet Base Dark
   - NemesisNet Base Light
   - NemesisNet Nemesis Dark
   - NemesisNet Nemesis Light
   - NemesisNet Aurora Dark
   - NemesisNet Aurora Light

### Alternative: Using Command Palette

1. Press `Ctrl+Shift+P` (or `Cmd+Shift+P` on macOS)
2. Type "Color Theme"
3. Select **"Preferences: Color Theme"**
4. Choose your preferred NemesisNet theme

## Publishing to VSCode Marketplace (Optional)

If you want to publish this theme to the VSCode Marketplace:

### Prerequisites

```bash
npm install -g @vscode/vsce
```

### Step 1: Update package.json

Add your publisher information:
```json
{
  "publisher": "your-publisher-name"
}
```

### Step 2: Package the Extension

```bash
cd NemesisNet-VSCode-Theme
vsce package
```

This creates a `.vsix` file you can:
- Install locally: `code --install-extension nemesisnet-theme-1.0.0.vsix`
- Publish to marketplace: `vsce publish`

### Step 3: Create Publisher Account

1. Go to https://marketplace.visualstudio.com/manage
2. Sign in with Microsoft/Azure account
3. Create a publisher
4. Get a Personal Access Token (PAT) from Azure DevOps

### Step 4: Publish

```bash
vsce login YOUR_PUBLISHER_NAME
vsce publish
```

## Troubleshooting

### Theme Not Showing Up

1. **Check folder location**: Ensure the folder is in the correct extensions directory
2. **Check folder name**: It should be `NemesisNet-VSCode-Theme` (or `nemesisnet-theme`)
3. **Reload VSCode**: Press `Ctrl+Shift+P` > "Developer: Reload Window"
4. **Check for errors**: Press `Ctrl+Shift+P` > "Developer: Toggle Developer Tools" > Console tab

### Colors Look Wrong

1. Make sure you don't have custom settings overriding the theme
2. Check `settings.json` for any `workbench.colorCustomizations`
3. Try with a fresh VSCode profile

### Syntax Highlighting Issues

1. Ensure the file language is correctly detected
2. Try reloading the window
3. Check if you have conflicting extensions

## Settings Recommendations

Add these to your `settings.json` for the best experience:

```json
{
  "editor.fontSize": 14,
  "editor.fontFamily": "'JetBrains Mono', 'Fira Code', 'Cascadia Code', Consolas, monospace",
  "editor.fontLigatures": true,
  "editor.lineHeight": 1.6,
  "editor.cursorBlinking": "smooth",
  "editor.cursorSmoothCaretAnimation": "on",
  "editor.smoothScrolling": true,
  "workbench.list.smoothScrolling": true,
  "terminal.integrated.smoothScrolling": true,
  "editor.bracketPairColorization.enabled": true,
  "editor.guides.bracketPairs": "active"
}
```

## Font Recommendations

For the best experience with NemesisNet themes, consider these fonts:

- **JetBrains Mono** - https://www.jetbrains.com/lp/mono/
- **Fira Code** - https://github.com/tonsky/FiraCode
- **Cascadia Code** - https://github.com/microsoft/cascadia-code
- **Victor Mono** - https://rubjo.github.io/victor-mono/

All support ligatures and are optimized for coding!

## Support

For issues or questions:
- Email: hello@nemesisnet.co.za
- GitHub: https://github.com/NemesisNet/vscode-theme/issues
