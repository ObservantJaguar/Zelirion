# Zelirion — Cross‑Platform Desktop Environment Meta‑Distribution

Zelirion is a multi‑platform meta‑distribution providing modern, lightweight, mobile‑friendly, and experimental Desktop Environments (DEs) across **Linux (Devuan)**, **FreeBSD**, and **illumos**.

The project focuses on portability, UNIX consistency, and DE availability across systems that traditionally lack modern desktop environments.

Zelirion delivers a unified build architecture for generating ISO images for multiple DEs on multiple UNIX‑like platforms, including touchscreen‑oriented environments and alternative shells.

---

## Project Status

Zelirion is currently in early development.

ISO images will be published once the build system and DE integration layers are complete.

---

## Goals

- Provide a consistent family of DE‑focused distributions across Linux, FreeBSD, and illumos.
- Support modern, lightweight, mobile, and experimental Desktop Environments.
- Avoid Linux‑specific lock‑in (systemd, Wayland‑only DEs).
- Maintain maximum portability using Devuan (elogind, eudev, sysvinit/OpenRC/runit).
- Adapt mobile DEs (Phosh, Plasma Mobile, Glacier, JingOS, Lomiri) for desktop and non‑Linux platforms.
- Port GSM/Modem stack (ModemManager, ofono, libqmi, libmbim) to FreeBSD and illumos.
- Provide a modular build system for generating ISO images per DE.
- Maintain a unified naming scheme where each build has a unique identity.

---

## Supported Platforms

### Linux (Devuan)
Classic UNIX architecture without systemd.  
Full X11 support, partial Wayland support.

### FreeBSD
Robust UNIX platform with full X11 support and partial Wayland support.

### illumos (OpenIndiana / OmniOS)
Solaris‑derived UNIX platform with full X11 support and no Wayland support.

---

## Supported Desktop Environments

Zelirion includes classic, modern, experimental, mobile, and lightweight DEs:

Xfce, Cinnamon, Deepin, LXQt, MATE, KDE Plasma, Budgie, UKUI, Trinity TDE, Lumina, EDE,  
CuteFish, Maui Shell, COSMIC, PaperDE, SonicDE, Liri,  
Phosh, Plasma Mobile, Glacier, JingOS, Lomiri,  
Enlightenment.

---

## Build Name Matrix — Linux (Devuan)

| Desktop Environment | Build Name |
|---------------------|------------|
| KDE Plasma | Aurora |
| Xfce | Zentora |
| LXQt | Quarisa |
| MATE | Verdina |
| Cinnamon | Cinnara |
| Deepin | Divira |
| Budgie | Avira |
| UKUI | Kalira |
| Enlightenment | Enlira |
| EDE | Edessa |
| Liri | Lirena |
| CuteFish | Cutora |
| Pantheon | Pantara |
| Lumina | Lumera |
| Trinity TDE | Trinira |
| SonicDE | Sonira |
| Plasma Mobile | Novara |
| Phosh | Fosira |
| Glacier | Glafira |
| Lomiri | Lomira |
| JingOS | Jingara |
| PaperDE | Papira |
| Maui Shell | Mauira |

---

## Build Name Matrix — FreeBSD

| Desktop Environment | Build Name |
|---------------------|------------|
| KDE Plasma | Crestara |
| Xfce | Valora |
| LXQt | Arlissa |
| MATE | Virelina |
| Lumina | Lumenia |
| Trinity TDE | Tavira |
| Enlightenment | Entrisa |
| UKUI | Kavera |
| EDE | Edrina |

---

## Build Name Matrix — illumos

| Desktop Environment | Build Name |
|---------------------|------------|
| KDE Plasma | Zalvira |
| Xfce | Arvessa |
| LXQt | Sylvira |
| MATE | Viresta |
| Trinity TDE | Solviera |

---

## Wayland and X11 Compatibility

### Linux (Devuan)
Wayland available via elogind.  
X11 fully supported.

### FreeBSD
Partial Wayland support.  
Full X11 support.

### illumos
No Wayland support.  
Full X11 support.

Wayland‑only DEs run in X11 fallback mode where Wayland is unavailable.

---

## Why Devuan

Devuan avoids systemd and provides:

- elogind  
- eudev  
- sysvinit / OpenRC / runit  
- full X11 support  
- partial Wayland support  

This makes Devuan ideal for cross‑platform DE portability.

---

## GSM / Modem Stack Ambition

Zelirion aims to support touchscreen DEs as full mobile environments on FreeBSD and illumos.

Planned components:

- ModemManager  
- ofono  
- libqmi  
- libmbim  
- SMS/USSD utilities  
- Call management  
- Mobile data stack  

---

## Repository Structure

```text
Zelirion/
 ├─ build/
 │   ├─ build-plasma.sh
 │   ├─ build-cinnamon.sh
 │   ├─ build-cosmic.sh
 │   ├─ build-phosh.sh
 │   ├─ build-enlightenment.sh
 │   └─ ...
 ├─ configs/
 │   ├─ base/
 │   ├─ installer/
 │   └─ platform/
 ├─ docs/
 │   ├─ wayland-support.md
 │   ├─ gsm-stack.md
 │   ├─ de-compatibility.md
 │   └─ build-system.md
 ├─ iso/
 │   └─ output/
 └─ README.md
```

```text
Each DE has its own repository:

Zelirion-Plasma
Zelirion-Cinnamon
Zelirion-COSMIC
Zelirion-CuteFish
Zelirion-MauiShell
Zelirion-Phosh
Zelirion-PlasmaMobile
Zelirion-Glacier
Zelirion-Enlightenment
Zelirion-LXQt
Zelirion-MATE
Zelirion-Deepin
Zelirion-UKUI
Zelirion-Lumina
Zelirion-EDE
Zelirion-TDE
Zelirion-PaperDE
Zelirion-SonicDE
Zelirion-Liri
```

---

## Roadmap

- Provide a consistent family of DE‑focused distributions across Linux, FreeBSD, and illumos.
- Support modern, lightweight, mobile, and experimental Desktop Environments.
- Avoid Linux‑specific lock‑in (systemd, Wayland‑only DEs).
- Maintain maximum portability using Devuan (elogind, eudev, sysvinit/OpenRC/runit).
- Build ARM64 distributions for smartphones and tablets using mobile‑oriented DEs (Phosh, Plasma Mobile, Glacier, JingOS, Lomiri).
- Port GSM/Modem stack (ModemManager, ofono, libqmi, libmbim) to FreeBSD and illumos.
- Provide a modular build system for generating ISO images per DE.
- Maintain a unified naming scheme where each build has a unique identity.

---

## License

GPL (version to be decided).

---

## Contributing

Zelirion welcomes contributions in:

- Desktop Environments  
- UNIX portability  
- FreeBSD / illumos  
- Mobile UI frameworks  
- GSM / modem stacks  
- Build systems  
- Packaging  
- Documentation  

---

## Contact

Project maintainer: Maxim  
Location: Frankfurt am Main, Germany  
Languages: Russian / English
