# Arch Linux Installation Guide

## Initial Setup

1. run the bbh config found here
   - `archinstall --config-url https://raw.githubusercontent.com/mirror-shades/bbh/main/config.json`
2. choose your partition layout
3. make a sudo user profile

## Post-Install Setup

### Networking

Connect to WiFi (if needed):

```bash
nmcli dev wifi list
nmcli dev wifi connect <SSID> password <password>
```

### Setup config

```
git clone https://github.com/mirror-shades/arch-config.git
sudo cp ./arch-config/* ~/.config
rm -r arch-config // for cleanup
```

### Display Manager

Enable ly display manager. This command only needs to be run once:

```bash
sudo systemctl enable ly
```

## Finished

You now have an extremely lightweight rice of hyperland to do whatever you want with. I recommend starting by opening the hyprland config file at `~/.config/hypr` and setting key bindings the way you prefer.

### Programs

- Ghostty (terminal)
- Helix (editor)
- Rofi (programs menu)

### Keybindings

`Super + n` new terminal

- q quit window
- space see programs menu
- [number] switch workspace
- shift + [number] switch window to workspace

## Additional steps

Some additional software which may be useful (this will be automated in the future)

### Yay

```bash
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si
```

### Internet

```bash
yay -S zen-browser-bin
```

### File Explorer

```bash
yay -S yazi
```
