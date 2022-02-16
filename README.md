# Laptop Setup

This repository is designed to contain files and steps to customize my computers. In this repo are dotfiles, as well as general UI preferences I find convenient.

## .vimrc

- Clone [vundle](https://github.com/VundleVim/Vundle.vim) and [powerline-fonts](https://github.com/vim-airline/vim-airline)
  - For powerline fonts in iTerm2, modify the fonts. go to `Preferences > Profiles > Text` and select `Use a different font for non-ASCII text` 

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

### Useful vscode extensions

- Remote - SSH
- Default language extensions (C/C++, Python, etc.)
- Rainglow (themes)
  - Dark, not contrast: Frontier
  - Contrast: Darkside Contrast
- GitLens

## Mac-specific

### .zshrc

- Install [oh-my-zsh](https://ohmyz.sh/#install)
- install [Powerlevel10k](https://github.com/romkatv/powerlevel10k/), alternative to powerline that's easier to customize (and works with oh-my-zsh)
  - to confiure: `p10k configure`
  - configuration: <details>
    
    - classic
    - unicode
    - light
    - 12-hr format
    - angled
    - sharp
    - flat tail
    - 2-line
    - dotted
    - no prompt frame
    - compact spacing
    - many icons
    - concise
    - ...
    <summary> (expand to see) </summary>
    </details>
     

## Ubuntu-specific
- Download "gnome-tweaks" and "Workspace Matrix"

### Terminal setup

- preferences: ensure that there's no max scroll line value
- ctrl-tab tab switching:
```
gsettings set org.gnome.Terminal.Legacy.Keybindings:/org/gnome/terminal/legacy/keybindings/ next-tab '<Primary>Tab'
gsettings set org.gnome.Terminal.Legacy.Keybindings:/org/gnome/terminal/legacy/keybindings/ prev-tab '<Primary><Shift>Tab'
```
