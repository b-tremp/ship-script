# ship

Deploy prototypes to a live URL in seconds.

Supports `.html`, `.jsx`, and folders. No config, no setup, no build tools.

## Install

**Requires:** Node.js ([download here](https://nodejs.org) if you don't have it — check with `node -v`)

```bash
curl -fsSL https://raw.githubusercontent.com/b-tremp/ship-script/main/ship -o /usr/local/bin/ship && chmod +x /usr/local/bin/ship
```

> If you get a permission error, run it with `sudo` in front.

## Usage

```bash
ship prototype.html                  # deploy an HTML file
ship app.jsx                          # deploy a React component
ship ./my-project/                    # deploy a folder
ship prototype.html --name my-demo    # custom URL: my-demo.surge.sh
```

The first time you run it, it will auto-install Surge (takes ~5 seconds). Surge will ask you to create a free account — just enter your email and pick a password.

When it's done, you'll get a live URL and it's automatically copied to your clipboard.

## Example

```
$ ship landing-page.html --name landing-v2

⚡ Deploying HTML: landing-page.html
Deploying...

✓ Live!

  https://landing-v2.surge.sh

  ✓ URL copied to clipboard
```

## Troubleshooting

**"command not found: ship"**
Run the install command again, or add this to your `~/.zshrc`:
```bash
export PATH="/usr/local/bin:$PATH"
```

**"permission denied"**
Use `sudo` when installing:
```bash
sudo curl -fsSL https://raw.githubusercontent.com/b-tremp/ship-script/main/ship -o /usr/local/bin/ship && sudo chmod +x /usr/local/bin/ship
```

**Surge asks for a domain**
Just type a name like `my-prototype.surge.sh` and hit Enter.

**Folder paths with spaces**
Use a backslash or quotes:
```bash
ship ~/Coding/My\ Project/
ship "$HOME/Coding/My Project/"
```
