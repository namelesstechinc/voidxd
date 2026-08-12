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
</p>

---

## How to deploy (on a panel — beginner friendly)
Here's the full walkthrough for that.

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

On most panels (Pterodactyl-based ones, which is the majority) there's no separate "Environment" tab — the variables live **inside the same Startup tab from Step 3**, just scroll down. Each one shows up as its own labeled box (e.g. a box labeled `SESSION_ID`) — click into the box and paste your value there, don't type `SESSION_ID=` in front of it, the label already says what it is.

If your panel does have a separate "Variables" tab instead, look there.

Add these:

| Variable | Value |
|---|---|
| `SESSION_ID` | paste the session id you got in Step 1 |
| `PREFIX` | `.` (or whatever symbol you want commands to start with) |
| `BOT_NAME` | `VOID XD` (or your own name for it) |

No `PHONE_NUMBER` needed if you already have a `SESSION_ID` — leave it out.

Don't forget to hit **Save** after entering them, before you start the server.

If your panel doesn't have a fields-based variables screen at all, you can instead open the **File Manager**, edit the `.env` file that's already there, and fill in the same values directly.

### Step 5 — Start it

Click **Start**. If your panel has a separate **Install** button, you can click that first, but it's not required anymore — the bot installs its own dependencies automatically on first run if they're missing.

### Step 6 — Check the console

Watch the console output. You should see the VOID XD banner, then a green "✅ SYSTEMS ONLINE" box once it connects. If you see red error text instead, screenshot it and send it to support (links at the bottom) — most issues are a missing or mistyped `SESSION_ID`.

### Step 7 — Test it

Send `.menu` to your bot's number on WhatsApp. If it replies, you're done.

---

<details>
<summary><b>Prefer a VPS or terminal? Click here</b></summary>

```
npm start
```
That's it — dependencies install themselves automatically on first run if `node_modules` isn't there yet. Just fill in your `SESSION_ID` (or `PHONE_NUMBER`) in the `.env` file before starting.

To keep it running in the background:
```
npm run pm2
```

</details>

## A few commands worth knowing

- `.getsession` — DMs you your Session ID again, any time.
- `.restart` — restarts the bot.
- `.botsettings` — see every setting/toggle in one place.
- `.setowner`, `.whoami` / `.whois` — manage ownership, look up a WhatsApp user.
- `.addsudo` / `.delsudo` — give or remove bot-admin access for other numbers.
- `.antidelete on/off`, `.antideletedm on/off`, `.antideletegc on/off` — recover deleted messages.
- `.setmenuimage`, `.setwatermark`, `.setbotname` — customize how your bot looks and what it's called.

## Need help?

- WhatsApp: [wa.me/2349114751172](https://wa.me/2349114751172)
- Telegram: [t.me/namelesstechinc](https://t.me/namelesstechinc)
- Support group: [t.me/voidr3aper](https://t.me/voidr3aper)
