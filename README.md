# RocketClient – Sileo/Cydia Repository

This is a **Sileo/Cydia package repository** for jailbroken iOS devices, hosted via GitHub Pages at:

```
https://angstvorfrauen.github.io/
```

This URL can be added directly in **Sileo** (or other compatible package managers such as Zebra/Installer) to browse and install the packages below.

## 📱 Adding the repo

1. Open Sileo
2. Go to **Sources** → **+**
3. Enter the following URL:
   ```
   https://angstvorfrauen.github.io/
   ```
4. Add the source and install packages

Or use this deep link directly from your browser:
```
sileo://source/https://angstvorfrauen.github.io/
```

## 📦 Included packages

| Package | Version | Architecture | Description |
|---|---|---|---|
| Flex 3 Beta | 1:3~Beta75 | arm | Tweak injection framework |
| ChromaHomeBarX | 0.4 | arm | RGB coloring for the HomeBar |
| EeveeSpotify | 6.2.1 / 6.2.2 | arm / arm64 | Spotify modification |
| GesturesXV | 1.6 | arm | iPhone X gestures for older iPhones (iOS 15) |
| Filza File Manager | 4.0.1-3 | arm | File manager |
| BatteryBuddy | 1.3.5 | arm | Battery indicator tweak |
| Atria | 1.4.1 | arm | Homescreen customization |
| SwiftProtobuf | 1.29.0 | arm / arm64 | Protobuf runtime library (dependency) |
| libcolorpicker | 1.6.9 | arm | Color picker library for developers (dependency) |

> For the current, complete list, check the [`Packages`](./Packages) file, or browse the source directly inside Sileo after adding it.

## 📂 Project structure

```
.
├── index.html          # Landing page for the repo (GitHub Pages)
├── index.css           # Styling for the landing page
├── Packages            # Package index (plain text)
├── Packages.gz          # Package index (gzip)
├── Packages.bz2         # Package index (bzip2)
├── Release              # Repo metadata
├── debs/                # The actual .deb packages
├── icons/               # Package icons
├── depictions/          # JSON depictions for Sileo (arm / arm64)
├── images/              # Banner and other graphics
├── icon.png / CydiaIcon.png / sileo.png  # Repo icons
└── update.sh            # Script to rebuild the package index
```

## 🔧 Updating the repository

After adding or changing a `.deb` package in the `debs/` folder, regenerate the package index:

```bash
./update.sh
```

The script:
1. deletes the old `Packages.gz` / `Packages.bz2`
2. generates a new `Packages` index from `./debs` using `dpkg-scanpackages`
3. compresses the index as `.gz` and `.bz2`

**Requirement:** `dpkg-dev` (for `dpkg-scanpackages`) must be installed, e.g. on Debian/Ubuntu:
```bash
sudo apt install dpkg-dev
```

## ⚠️ Note

This repository is intended for users of **jailbroken iOS devices**. Jailbreaking removes security restrictions imposed by Apple and can affect device security and warranty. Use at your own risk. For questions or support, see the contact links below.

## 🔗 Contact / Links

- Telegram: [t.me/RocketClient2](https://t.me/RocketClient2)
- Website: [xeuka.net](https://xeuka.net)

## 📄 License

No license is specified in this project. Please contact the repo owner before reusing any packages or content.
