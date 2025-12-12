# Bash Configuration Setup

## Overview
A custom `.bashcfg` file to enhance the bash experience on Debian-based systems with aliases and settings for navigation, Git, Bun, and NPM.

## First-Time Setup
1. Copy the `.bashcfg` file to your home directory:
   ```bash
   touch ~/.bashcfg # then copy-paste the contents.
   ```
2. Run the following command to source the custom configurations via `.bashrc`:
   ```bash
   echo "source ~/.bashcfg" >> ~/.bashrc
   ```
3. Open a new shell or run following to apply changes:
   ```bash
   source ~/.bashrc
   ```

## Command Descriptions
- **General Aliases**:
  - `b`: Move up one directory and list contents (`cd .. && ls -lh`).
  - `r`: Go to root directory and list contents (`cd / && ls -lh`).
  - `h`: Go to home directory and list contents (`cd ~ && ls -lh`).
  - `ver`: Display OS release info (`cat /etc/os-release`).
  - `del`: Delete files/directories recursively (`rm -rf`).
  - `d`: Go to Desktop directory (`cd ~/Desktop`).
  - `brc`: Edit `.bashrc` with `kate` editor.
  - `aptup`: Update and upgrade Debian packages (`sudo apt-get update && sudo apt update && sudo apt upgrade`).
  - `c`, `cls`: Clear terminal screen (`clear`).
  - `t`: Display directory tree (`tree`).
  - `tg`: Display directory tree ignoring `.gitignore` files (`tree --gitignore`).
  - `q`: Exit terminal session (`exit`).
  - `scr`: Reload `.bashrc` and confirm (`source ~/.bashrc && echo ".bashrc reloaded!"`).

- **Git Aliases**:
  - `ginit`: Initialize Git repository with main branch (`git init -b main`).
  - `gc`: Clone a Git repository (`git clone`).
  - `gs`: Show Git status (`git status`).
  - `gb`, `gbv`, `gbr`, `gba`: List branches (`git branch`, with verbose, remote, or all options).
  - `gsa`: Show detailed Git status (`git status -uall`).
  - `gall`: Stage all changes, commit, and push (`git status -uall && git add . && noto -a && git push`).
  - `gsw`: Switch branches (`git switch`).
  - `gr`, `grh`, `grhh`: Reset Git changes (`git reset`, hard reset, or hard reset to HEAD).
  - `gpl`: Pull from remote (`git pull`).
  - `gps`, `gpsf`: Push to remote (`git push`, or force push).
  - `github`: Open GitHub Desktop (`github-desktop`).

- **Bun Aliases**:
  - `binit`: Initialize Bun project (`bun init`).
  - `bi`: Install Bun dependencies (`bun install`).
  - `br`, `brd`, `brb`, `brs`, `bra`, `bri`, `brw`: Run Bun scripts (`bun run`, for dev, build, start, android, ios, or web).

- **NPM Aliases**:
  - `ninit`: Initialize NPM project (`npm init`).
  - `ni`: Install NPM dependencies (`npm install`).
  - `nr`, `nrd`, `nrb`, `nrs`: Run NPM scripts (`npm run`, for dev, build, or start).

## Notes
- Ensure `kate`, `bun`, `git`, and `npm` are installed for full functionality.
- Edit `~/.bashcfg` to customize aliases or settings.
- The `~/.bashrc` file remains minimal, only sourcing `~/.bashcfg`.
