<div align="center">

# 🐭 BigLinux Community XFCE Config

**The Definitive XFCE Session for BigLinux Community Edition**

[![License: GPL-3.0](https://img.shields.io/badge/License-GPL--3.0-blue.svg?style=for-the-badge)](LICENSE)
[![XFCE](https://img.shields.io/badge/XFCE-2284F2?style=for-the-badge&logo=xfce&logoColor=white)](https://xfce.org/)
[![Arch Linux](https://img.shields.io/badge/Arch_Linux-1793D1?style=for-the-badge&logo=arch-linux&logoColor=white)](https://archlinux.org/)

</div>

---

## 📖 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Project Structure](#-project-structure)
- [Key Components](#-key-components)
- [Development](#-development)
- [Contributing](#-contributing)
- [License](#-license)

---

## 📋 Overview

The **comm-xfce-config** package delivers a highly optimized XFCE experience for BigLinux Community users. Known for its speed and low resource usage, this configuration ensures that XFCE looks modern and behaves correctly from the very first login, inheriting all installer preferences.

---

## 🚀 Features

- **Lightweight Speed**: Optimized configurations that respect XFCE's minimal footprint.
- **Smart Inheritance**: Automatically applies Language and Keyboard settings from the installer.
- **Modern Look**: Applies BigLinux themes and icons for a cohesive visual identity.
- **Hardware Ready**:
  - Configures **JamesDSP** for audio.
  - Sets appropriate GTK4 rendering defaults.

---

## 📁 Project Structure

```tree
comm-xfce-config/
├── pkgbuild/                 # Arch Linux packaging files
└── usr/bin/
    └── startxfce-community   # The session bootstrap script
```

---

## 🔧 Key Components

### `startxfce-community`

This script is the entry point for the session, performing:

1.  **Session Config**: Exports XFCE and GTK environment variables.
2.  **Localization**: Applies the system locale defined in `/etc/big-default-config/`.
3.  **Input Tuning**: Configures keyboard layouts.
4.  **Audio**: Activates JamesDSP if the user requested it during installation.

---

## 🛠️ Development

### Building the Package

```bash
cd pkgbuild
makepkg -si
```

### Testing

Run the startup script in debug mode to verify logic:

```bash
# Debug run with verbose output
bash -x /usr/bin/startxfce-community
```

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/amazing-feature`).
3. Commit your changes (`git commit -m 'Add amazing feature'`).
4. Push to the branch (`git push origin feature/amazing-feature`).
5. Open a Pull Request.

---

## 📄 License

Distributed under the **GPL-3.0 License**. See [LICENSE](LICENSE) for more information.
