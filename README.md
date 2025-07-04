## AdvancedKick

### AdvancedKick is a secure and modern kick system for FiveM. It allows authorized staff to kick players using a permission-based system with license validation. The script includes a sleek ox\_lib interface, predefined and custom kick reasons, and optional Discord webhook logging.

### Features

* **License-based Permissions** – Only specified licenses in `config.lua` can use `/kick`
* **Custom Kick Reasons** – Predefined reasons plus the ability to enter a custom one
* **Discord Webhook Support** – Log kick actions to your Discord server
* **Server-side Validation** – Protects against event abuse
* **Optimized with ox\_lib** – Uses `lib.inputDialog` and `lib.notify` for a smooth experience

---

### Installation

1. Download the resource and extract it into your server’s `resources` folder.
2. Add `ensure AdvancedKick` to your `server.cfg`.
3. Configure your staff permissions in `config.lua` by adding their license identifiers under `Config.KickPerms`.
4. Set your Discord webhook URL in `config.lua` for logging (optional).

---

### Configuration Example (`config.lua`)

```lua
Config.KickPerms = {
    ["license:abc123..."] = true,
    ["license:def456..."] = true,
}

Config.Webhook = "https://your-webhook-url-here"
```

---

### Commands

* `/kick` – Opens the kick menu for authorized staff

---

### Dependencies

* [ox\_lib](https://overextended.dev/ox_lib)

---

### Notes

* Unauthorized users attempting to run `/kick` will receive a permission denied notification.
* Server-side checks ensure only valid licenses can execute kicks.
