# Steam Session for Linux

## Purpose
This project provides a minimal desktop session for Linux display managers (such as SDDM), allowing users to log in directly to Steam in Big Picture mode. The session is designed for gaming setups, living room PCs, or dedicated gaming machines where the primary use is running Steam and games, without the overhead of a full desktop environment.

## Main Advantage
Unlike standard desktop sessions, this session launches only Steam (in Big Picture mode) and the selected game. No additional background services, desktop panels, or unused applications are started, resulting in:
- Lower resource usage
- Faster startup
- Reduced potential for distractions or conflicts
- A more console-like experience

## How it works
After installation, a new session called "Steam (Big Picture)" will appear in your display manager's session list. Selecting this session will:
- Start Steam in Big Picture mode
- Allow you to launch games directly
- Avoid starting unnecessary desktop services

## Requirements
- Steam (recommended dependency)

## Installation
Install the package and select the "Steam (Big Picture)" session from your login screen.

### Repository Sources

To install from the Vitex Software repository, add the following to your APT sources:



```shell
sudo apt install lsb-release wget apt-transport-https bzip2


wget -qO- https://repo.vitexsoftware.com/keyring.gpg | sudo tee /etc/apt/trusted.gpg.d/vitexsoftware.gpg
echo "deb [signed-by=/etc/apt/trusted.gpg.d/vitexsoftware.gpg]  https://repo.vitexsoftware.com  $(lsb_release -sc) games" | sudo tee /etc/apt/sources.list.d/vitexsoftware-games.list
sudo apt update
sudo apt install steam-session
```

# For Debian Trixie and newer, you can use the following sources list entry:

/etc/apt/sources.list.d/vitexsoftware.sources

```shell
Types: deb
URIs: https://repo.vitexsoftware.com/
Suites: trixie
Components: games
Signed-By: /etc/apt/trusted.gpg.d/vitexsoftware.gpg
```
