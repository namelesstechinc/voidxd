<p align="center">
  <img src="./voidmedia/banner.jpg" width="380" alt="VOID XD">
</p>
<h1 align="center">VOID XD</h1>
<p align="center">WhatsApp bot powered by <b>Nameless Tech</b> — deploy your own with a Session ID, no code editing required.</p>
<p align="center">
  <a href="https://github.com/namelesshimself/voidxd/fork">
    <img src="https://img.shields.io/badge/Fork-Repository-2563eb?style=for-the-badge&logo=github&logoColor=white" alt="Fork Repository">
  </a>
  <a href="https://voidxd.namelesstech.space">
    <img src="https://img.shields.io/badge/Get-Session%20ID-7c5cff?style=for-the-badge&logo=whatsapp&logoColor=white" alt="Get Session ID">
  </a>
  <a href="https://youtu.be/o9MXDp6aDkQ">
    <img src="https://img.shields.io/badge/Watch-Tutorial-ff0000?style=for-the-badge&logo=youtube&logoColor=white" alt="Watch Tutorial">
  </a>
</p>

---

## How to deploy (on a panel — beginner friendly)

📺 **[Watch the full video tutorial here](https://youtu.be/o9MXDp6aDkQ)** — or follow the written walkthrough below.

### Step 1 — Get your Session ID first
Before touching your panel, go to **[voidxd.namelesstech.space](https://voidxd.namelesstech.space)**, enter your WhatsApp number, and link the device using the code it gives you. Your Session ID gets DMed straight to your own WhatsApp — copy it from there and keep it somewhere safe. You'll need it in Step 4.

### Step 2 — Get the bot files onto your panel
- Download this repo as a ZIP (green "Code" button on GitHub → "Download ZIP"), **or** if your panel supports it, use its "Deploy from GitHub" / "Import" option and paste the repo link directly.
- If you downloaded a ZIP: open your panel's **File Manager**, upload the ZIP into the server's root folder, then use the panel's "Unarchive"/"Extract" option on it. Delete the ZIP afterward if it's still there.
- When you're done, the root folder of your server should show `void.js`, `index.js`, `package.json`, and the rest of the files directly — not sitting inside an extra folder.

### Step 3 — Set the startup file
In your panel's **Startup** (or "Settings") tab:
- Set the **Main File** / **Entry Point** to `index.js`
- If it asks for a start command instead, use `node index.js` or `npm start`
- Make sure it's running **Node.js 18 or newer**

### Step 4 — Add your environment variables
Navigate to the `.env` file, edit it, and fill in your values (`SESSION_ID`, `PREFIX`, `BOT_NAME`, etc.).

### Step 5 — Install and start
- Click **Install** (most panels run `npm install` automatically the first time — if yours doesn't, find a button or console command for it)
- Once install finishes, click **Start**

### Step 6 — Check the console
Watch the console output. You should see the VOID XD banner, then a green "✅ SYSTEMS ONLINE" box once it connects. If you see red error text instead, screenshot it and send it to support (links at the bottom) — most issues are a missing or mistyped `SESSION_ID`.

### Step 7 — Test it
Send `.menu` to your bot's number on WhatsApp. If it replies, you're done.

---

<details>
<summary><b>Prefer a VPS or terminal? Click here</b></summary>

```
npm install --legacy-peer-deps
```

Edit your `.env` file:

```
SESSION_ID=paste-your-session-id-here
PREFIX=.
BOT_NAME=VOID XD
```

Then:

```
npm start
```

or, to keep it running in the background:

```
npm run pm2
```

</details>

## A few commands worth knowing
- `.getsession` — DMs you your Session ID again, any time.
- `.restart` — restarts the bot.
- `.addsudo` / `.delsudo` — give or remove bot-admin access for other numbers.
- `.antidelete on/off`, `.autoview on/off`, `.autoaza on/off` — toggle features on or off.
- `.setmenuimage`, `.setvvtext` — customize your bot's menu image and view-once watermark.

## Need help?
- 📺 Video tutorial: [youtu.be/o9MXDp6aDkQ](https://youtu.be/o9MXDp6aDkQ)
- WhatsApp: [wa.me/2349114751172](https://wa.me/2349114751172)
- Telegram: [t.me/namelesstechinc](https://t.me/namelesstechinc)
- Support group: [t.me/voidr3aper](https://t.me/voidr3aper)
