# My Tmux Configuration

A streamlined, robust `tmux` configuration optimized for productivity. Features custom prefix bindings, vi-mode navigation, and a dynamic multi-OS clipboard configuration.

## Key Features

- **Prefix:** Changed from `C-b` to `C-p` for improved ergonomics.
- **Navigation:** Native `vi-mode` keys for pane switching and buffers.
- **Status Bar:** Highly legible layout utilizing a solid blue background.
- **Clipboard Sync:** Smart OS detection that automatically routes copies to `pbcopy` on macOS or `xclip` on Linux.

---

## Installation (On a New Machine)

To deploy this configuration on a new machine, follow these steps:

### 1. Prerequisites

Ensure `tmux` is installed. If you are on Linux and want system clipboard synchronization, install `xclip`:

```bash
# Ubuntu / Debian
sudo apt update && sudo apt install xclip tmux -y

# macOS
brew install tmux

```

### 2. Clone the Repository

Clone this repository directly into your home directory:

```bash
git clone git@github.com:igor17400/my_tmux_cfg.git ~/my_tmux_cfg

```

### 3. Create a Symbolic Link

Create a symlink pointing from the default Tmux config path to your cloned repository.
_(Note: If an existing `.tmux.conf` file is present, remove or back it up first)._

```bash
# (Optional) Backup an existing config if present
[ -f ~/.tmux.conf ] && mv ~/.tmux.conf ~/.tmux.conf.bak

# Create the symlink
ln -s ~/my_tmux_cfg/tmux.conf ~/.tmux.conf

```

### 4. Load the Configuration

If Tmux is already running, resource the fil

```bash
tmux source-file ~/.tmux.conf

```

Alternatively, simply start a new session by running:

```bash
tmux

```

---

## Core Keybindings Reference

| Action                          | Shortcut        |
| ------------------------------- | --------------- |
| **Prefix Key**                  | `Ctrl + p`      |
| **Reload Config**               | `Prefix` -> `r` |
| **Enter Copy Mode**             | `Prefix` -> `[` |
| **Begin Selection (Copy Mode)** | `v`             |
| **Yank Selection (Copy Mode)**  | `y`             |
| **Paste Buffer**                | `Prefix` -> `P` |
