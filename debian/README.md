Bash Configuration
Overview
This repository contains a customized .bashrc file for Debian-based systems, enhancing the terminal experience with aliases, prompt settings, and environment configurations.
Features

History Management: Ignores duplicate commands and commands starting with a space; appends to history file.
Prompt Customization: Configures a colorized prompt based on terminal capabilities and sets terminal title for xterm.
Window Size Check: Updates LINES and COLUMNS after each command.
Color Support: Enables color for ls and other commands via dircolors.
Aliases:
General: Navigation (b, r, h, d), file management (del, ll, la, l), and system utilities (aptup, ver, scr).
Git: Repository management (ginit, gc, gs, gb, etc.) and workflow (gall, gpl, gps).
Bun: Project initialization and management (binit, bi, br, brd, etc.).
NPM: Node.js project commands (ninit, ni, nr, nrd, etc.).


Environment Variables:
Sets EDITOR to kate.
Configures BUN_INSTALL and adds Bun to PATH.


Completion: Enables programmable bash completion if available.

Installation

Clone the repository:git clone <repository-url>


Copy .bashrc to your home directory:cp bashrc/debian/.bashrc ~/.bashrc


Source the file to apply changes:source ~/.bashrc



Usage

Use aliases for quick navigation, git operations, or package management.
Customize the .bashrc file further by editing with brc alias (kate ~/.bashrc).
Reload changes with scr alias (source ~/.bashrc).

Notes

Ensure ~/.bash_aliases exists if additional aliases are defined.
Some features (e.g., lesspipe, globstar) are commented out; uncomment to enable.
Requires dircolors, bash-completion, and other standard Debian utilities for full functionality.
