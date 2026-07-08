# Pandora Launcher (Offline Edition)

[Pandora Launcher](https://github.com/Moulberry/PandoraLauncher) is one of the best Minecraft launchers written in Rust, packed with incredibly cool features. Check out the original repository for all the details!

I got tired of dealing with questionable Russian forks just to play offline. I wanted something clean, fast, and honest.

So I made this fork. 

It is a fully automated, transparent offline version. The entire "crack" is literally just removing 4 lines of code that force a Microsoft account login in UI. That's it :)

---

## Downloads & Installation

You can always find the latest automatically built files on the [Releases](https://github.com/Max-pro273/PandoraLauncherOffline/releases/latest) page. Just copy and paste these commands to install (make sure to replace the filenames with the exact ones from the latest release):

### Linux
**Debian / Ubuntu** (`.deb`):
```bash
wget https://github.com/Max-pro273/PandoraLauncherOffline/releases/latest/download/PandoraLauncher-Linux-x86_64.deb
sudo apt install ./PandoraLauncher-Linux-x86_64.deb
```

**Fedora / RHEL** (`.rpm`):
```bash
sudo dnf install https://github.com/Max-pro273/PandoraLauncherOffline/releases/latest/download/PandoraLauncher-Linux-x86_64.rpm
```

**Arch Linux** (`.pacman`):
```bash
sudo pacman -U https://github.com/Max-pro273/PandoraLauncherOffline/releases/latest/download/PandoraLauncher-Linux-x86_64.pacman --config <(echo -e "[options]\nRemoteFileSigLevel = Optional")
```

**Universal** (`.AppImage`): 
```bash
wget https://github.com/Max-pro273/PandoraLauncherOffline/releases/latest/download/PandoraLauncher-Linux-x86_64.AppImage
chmod +x PandoraLauncher-Linux-x86_64.AppImage
./PandoraLauncher-Linux-x86_64.AppImage
```

### Windows
Download the `-Setup.exe` or `-Portable.exe` directly from the [Releases](https://github.com/Max-pro273/PandoraLauncherOffline/releases/latest) page.

### macOS
Download the `.dmg` or portable version directly from the [Releases](https://github.com/Max-pro273/PandoraLauncherOffline/releases/latest) page.

## Usage for Original Launcher (Offline Bypass)

If you prefer to use the **unmodified original launcher**, you can still unlock the offline feature by manually injecting a placeholder account file.

Download the original launcher, run it, **close the launcher**, then execute the appropriate command for your os:

**Windows CMD:**
```cmd
echo {"accounts": {"00000000-0000-0000-0000-000000000000": {"username": "OfflinePlayer","offline": true,"head": null}},"selected_account": "00000000-0000-0000-0000-000000000000"} > %appdata%\PandoraLauncher\accounts.json
```

**Windows PowerShell:**
```powershell
'{"accounts": {"00000000-0000-0000-0000-000000000000": {"username": "OfflinePlayer", "offline": true, "head": null}}, "selected_account": "00000000-0000-0000-0000-000000000000"}' | Out-File -FilePath "$env:APPDATA\PandoraLauncher\accounts.json" -Encoding utf8 -Force
```

**Linux Shell:**
```bash
echo '{"accounts": {"00000000-0000-0000-0000-000000000000": {"username": "OfflinePlayer","offline": true,"head": null}},"selected_account": "00000000-0000-0000-0000-000000000000"}' > ~/.local/share/PandoraLauncher/accounts.json
```

**macOS:**
```bash
echo '{"accounts": {"00000000-0000-0000-0000-000000000000": {"username": "OfflinePlayer","offline": true,"head": null}},"selected_account": "00000000-0000-0000-0000-000000000000"}' > ~/Library/Application\ Support/PandoraLauncher/accounts.json
```

## ❤️ Credits
Huge thanks to [Moulberry](https://github.com/Moulberry) for creating the amazing original Pandora Launcher. All credit for the core launcher belongs to them.

*Made in Ukraine 🇺🇦*
