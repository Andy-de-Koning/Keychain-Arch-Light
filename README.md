# Keychain-Arch-Light

Een minimalistisch, razendsnel Bash-script voor het beheren van SSH-agents op Arch Linux. Specifiek ontworpen voor tiling window managers zoals Hyprland en moderne shells zoals Zsh.

## Waarom Keychain-Arch-Light?
De originele `keychain` is fantastisch, maar bevat veel "legacy code" voor antieke systemen (Solaris, HP-UX, etc.). Dit script is een "one-shot" utility:
- **Lichtgewicht:** Geen overbodige checks voor systemen uit de jaren '90.
- **Snel:** Gebruikt ingebouwde shell-variabelen in plaats van externe commando's.
- **CPU-vriendelijk:** Geen achtergrondprocessen of oneindige loops; het script voert zijn taak uit en sluit direct af.
- **Arch-native:** Geen afhankelijkheid van `inetutils` (hostname).


## Installatie via AUR (Aanbevolen voor Arch gebruikers)
Gebruik je favoriete AUR-helper (zoals `yay` of `paru`):
```bash
yay -S keychain-arch-light
```

## Installatie

### 1. Clone de repository:
   ```bash
   git clone https://github.com/andy-de-koning/keychain-arch-light.git
   ```
### 2. Maak het script uitvoerbaar:

```bash
chmod +x keychain
```
### 3. Verplaats het naar je lokale bin-map:

```bash
mkdir -p ~/.local/bin
cp keychain ~/.local/bin/
```
## Gebruik
Voeg de volgende regel toe aan je .zshrc of .bashrc:

```bash
eval $(~/.local/bin/keychain --eval --agents ssh id_rsa)
```

