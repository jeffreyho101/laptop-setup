# Laptop Setup

This repository is designed to contain files and steps to customize my computers. In this repo are dotfiles, as well as general UI preferences I find convenient.

## Ubuntu Setup
- Download "gnome-tweaks" and "Workspace Matrix"

### Terminal setup

- preferences: ensure that there's no max scroll line value
- ctrl-tab tab switching:
```
gsettings set org.gnome.Terminal.Legacy.Keybindings:/org/gnome/terminal/legacy/keybindings/ next-tab '<Primary>Tab'
gsettings set org.gnome.Terminal.Legacy.Keybindings:/org/gnome/terminal/legacy/keybindings/ prev-tab '<Primary><Shift>Tab'
```

## VSCode

Keybindings - switching tabs in a cycle with ctrl-tab:
- create file `~/.config/Code/User/keybindings.json` wherever the VSCode config lies, and add the following:
```
[
    {
        "key": "ctrl+tab",
        "command": "workbench.action.nextEditorInGroup"
    },
    {
        "key": "ctrl+shift+tab",
        "command": "workbench.action.previousEditorInGroup"
    }
]
```
