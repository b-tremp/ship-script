# ship

Turn any prototype into a live URL you can share — in seconds.

No build tools, no deploys, no asking engineering. Just one command.

---

## One-time setup (5 minutes)

### 1. Make sure you have Node.js

Open **Terminal** (search "Terminal" in Spotlight) and paste this:

```
node -v
```

If you see a version number like `v20.11.0` — you're good, skip to step 2.

If you see `command not found` — download Node.js first:
1. Go to [nodejs.org](https://nodejs.org)
2. Click the big green **Download** button
3. Open the installer and follow the steps
4. Restart Terminal, then try `node -v` again

### 2. Install ship

Paste this entire line into Terminal and hit Enter:

```
curl -fsSL https://raw.githubusercontent.com/b-tremp/ship-script/main/ship -o /usr/local/bin/ship && chmod +x /usr/local/bin/ship
```

**If you see "Permission denied"**, paste this version instead (it will ask for your Mac password):

```
sudo curl -fsSL https://raw.githubusercontent.com/b-tremp/ship-script/main/ship -o /usr/local/bin/ship && sudo chmod +x /usr/local/bin/ship
```

### 3. Verify it worked

```
ship
```

You should see the help text. You're all set!

---

## How to use it

### Deploy an HTML file

```
ship my-prototype.html
```

### Deploy a folder

```
ship ./my-project/
```

### Pick a custom URL

```
ship my-prototype.html --name cool-demo
```

This gives you → `https://cool-demo.surge.sh`

### Deploy a React (.jsx) file

```
ship app.jsx
```

---

## What to expect the first time

1. Ship will auto-install Surge (a free hosting service) — takes about 5 seconds
2. Surge will ask for your **email** and a **password** — just make one up, it's a free account
3. You'll get a live URL and it's **automatically copied to your clipboard**

After the first time, deploys take a couple seconds.

---

## Example

```
$ ship landing-page.html --name landing-v2

⚡ Deploying HTML: landing-page.html
Deploying...

✓ Live!

  https://landing-v2.surge.sh

  ✓ URL copied to clipboard
```

---

## Common issues

**"command not found: ship"**

The install didn't stick. Paste the install command from step 2 again.

**It's asking me for a domain**

Type a name ending in `.surge.sh` and hit Enter. Example: `my-prototype.surge.sh`

**Folder name has spaces in it**

Put the path in quotes:

```
ship "$HOME/Coding/My Project/"
```

**"Permission denied" during install**

Use the `sudo` version of the install command from step 2. It will ask for your Mac login password (you won't see the characters as you type — that's normal, just type it and hit Enter).
