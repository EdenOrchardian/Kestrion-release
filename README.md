# Kestrion

**A real-time strategy game where you design every ship you command.**

Build ships block by block on a grid (hulls, armour, engines, reactors, shields and weapons from autoguns to railguns, torpedoes, drones and lightning), put them into fleets, then lead those fleets into battle against the AI or your friends.

This repository is where the **Stable** releases of Kestrion are published. The game's own updater reads from here, and you can download the game here too.

## Download

**[Get the latest version](https://github.com/EdenOrchardian/Kestrion-release/releases/latest)**, then under **Assets**:

- **`Kestrion-<version>-setup.exe`**: the installer (recommended).
  - **Express** installs straight away into your own user folder.
  - **Custom** lets you choose the folder and the shortcuts.
  - No administrator rights needed.
- **`Kestrion-<version>-win-x64.zip`**: the portable version. Unzip it anywhere and run `Kestrion.exe`.

**Windows will say "Windows protected your PC".** That happens because the installer is not signed with a paid Windows certificate yet, not because anything is wrong with it. Click **More info**, then **Run anyway**. To be sure a file really is ours, see [Checking your download](#checking-your-download).

**Requirements:** Windows 10 or 11 (64-bit). A Linux version is planned.

## Updates

Once installed, Kestrion keeps itself up to date from this page:

- It **always asks before downloading** anything, and never interrupts a match.
- It installs when you close the game, or when you press **Restart now**.
- The previous version is always kept. **Settings > Updates > Go back to the previous version** takes you back at any time. If a new version fails to start twice in a row, the game offers to go back for you.
- **An update check sends nothing about you**: it is one plain download of a small file from this page. You can switch update checks off in **Settings > Updates**.
- Multiplayer needs everyone on the same version, so update before playing with friends.

## What we are building

Kestrion is made by **EdenOrchardian**, one developer with a clear idea of what this game should be:

- **Your designs, your tactics.** The ship you fly is the ship you built. Winning should come from good designs and good decisions, not from grinding or paying.
- **An AI that never cheats.** Computer opponents only see and do what a player could. Harder levels think better; they don't get extra money or see through fog.
- **Fair, smooth multiplayer.** Every player's game runs the exact same simulation, so what you see is what happened. Play directly with friends, with no account needed.
- **Your privacy and safety come first.** No trackers, no ads, no data collection. **Hide my IP** keeps your address hidden from other players. Updates are signed so nobody else can slip something onto your PC. Every feature that touches the internet gets a security review before it ships.
- **Player experience first.** Clear screens, plain words, no dark patterns.

What's on the way: balance and polish, a Linux version, a website, more weapons and maps, mod support, Steam, and later a campaign.

## Why Kestrion is made with AI

I have always wanted to build a game of my own. What stopped me was never the ideas. It was time, and the expertise to turn an idea into something real, polished and safe to put on other people's computers.

Kestrion is made with **Claude**, Anthropic's AI, as a working partner. I have watched AI tools get misused: flooding shops with low-effort copies, standing in for artists, shipping things nobody checked. I want to show the other way. Here is how AI is used properly, as a tool, to make something interesting and unique that could not have existed otherwise:

- **The vision and every decision are mine.** What the game is, how it plays, how it looks and what it will never do. The AI builds, I direct, and nothing ships without my say.
- **Nothing is taken from other people's work.** The game's art is drawn by code, designed and refined in rounds of mockups that I choose from, not generated images.
- **Everything is tested before it reaches you.** Automated checks, live play tests on real machines, and a full security review of everything that touches the internet.
- **I'm open about it.** You are reading this.

If Kestrion turns out good, it will be because a person with a clear idea had the right tool, and used it with care.

## Checking your download

Every file is listed in **`SHA256SUMS.txt`** and signed with our release key in the standard **minisign** format.

**Our public key** (key id `6B4826021ADD7830`):

```
RWQweN0aAiZIa/zdL8dDf65GIuVV6kkLvVnUnoUITMVKKxAEHaMgN+t8
```

Check a file's hash in PowerShell, and compare the result with the matching line in `SHA256SUMS.txt`:

```
Get-FileHash .\Kestrion-<version>-setup.exe -Algorithm SHA256
```

Or check the signature with [minisign](https://jedisct1.github.io/minisign/):

```
minisign -Vm Kestrion-<version>-setup.exe -P RWQweN0aAiZIa/zdL8dDf65GIuVV6kkLvVnUnoUITMVKKxAEHaMgN+t8
```

The same key is shown in the game's Beta repository and on our website. **If the key you see anywhere ever differs from this one, do not run the file, and tell us.**

## Beta

Want new features before everyone else? Testers get early builds from the [Beta channel](https://github.com/EdenOrchardian/Kestrion-dev). Ask for the Beta code on our Discord, then type it in **Settings > Updates**.

## Feedback and bugs

Tell us on our Discord: what you did, what happened, and your version (shown in **Settings**). If a multiplayer match falls out of sync, the game saves a small `.kdesync` report you can send us.

---

*This repository only holds releases. The game's source code is not public.*
