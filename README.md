# VS Code Customization

A reusable VS Code workspace configuration

## Included

- `.vscode/settings.json` - editor, terminal, Git, UI, performance, and language settings
- `.vscode/extensions.json` - recommended extensions for the workflow

## Reuse In Any Repository

Copy the `.vscode` directory into the project you want to configure:

```bash
cp -R .vscode /path/to/your-project/
```

Or clone this repository and copy the configuration:

```bash
git clone <repository-url> vscode-setup
cp -R vscode-setup/.vscode /path/to/your-project/
```

Open the target project in VS Code, then run:

1. `Extensions: Show Recommended Extensions`
2. Install the workspace recommendations
3. `Developer: Reload Window`

### Extensions

To export currently installed extensions:

```bash
code --list-extensions > extensions-installed.txt
```

To install an exported list later:

```bash
while read -r extension; do code --install-extension "$extension"; done < extensions-installed.txt
```

Todo Tree uses the installed remote ripgrep binary through `todo-tree.ripgrep.ripgrep`.
On this Linux setup, the configured path is `/usr/bin/rg` or for Mac use `/opt/homebrew/bin/rg`.

Install these locally:

- GitHub Dark theme
- Material Icon Theme
- Custom UI Style
