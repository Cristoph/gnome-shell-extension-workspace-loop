# Gnome Extension Workspace Loop 🔄

⚠️ **WORK IN PROGRESS** ⚠️

**Workspace Loop** is a minimalist, single-purpose GNOME Shell extension designed to eliminate the linear navigation constraint of native workspaces.

---

## The Problem
* By default, GNOME treats workspaces as a finite line with fixed boundaries.
* When you reach the last workspace, standard navigation commands (such as `switch-to-workspace-right`) stop functioning instead of returning to the start.
* There is no official setting within `gsettings` or `dconf` to enable a wrap-around behavior.

## The Solution
This extension intercepts workspace navigation and applies a modulo operation to ensure a seamless, infinite loop.
* **100% Native:** Implemented using GJS (GNOME JavaScript) to interact directly with `global.workspace_manager`.
* **Zero Dependencies:** It eliminates the need for XWayland or external Python scripts, functioning natively within the Shell.
* **Modern Architecture:** Built using ESM (ECMAScript Modules) to ensure compatibility with GNOME 45 through GNOME 50.

## Key Features
* **Infinite Cycling:** Jump from the last workspace to the first and vice-versa without interruption.
* **Native Integration:** Uses Libadwaita for a clean preferences interface that matches the modern GNOME aesthetic.
* **Custom Keybindings:** Easily configure your preferred shortcuts directly within the extension settings, replacing manual `gsettings` hacks.
* **Lightweight:** Designed to be "invisible"—it runs with near-zero resource overhead.

## Installation

1. Clone this repository into your local extensions directory:
   ```bash
   git clone [https://github.com/tu-usuario/gnome-shell-extension-workspace-loop.git](https://github.com/tu-usuario/gnome-shell-extension-workspace-loop.git) ~/.local/share/gnome-shell/extensions/workspace-loop@cris.local
