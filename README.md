# fsmentor
CLI for the Linux filesystem, Debian packages. Explains the FHS, paths, commands and packages in plain language.
fsmentor – File System Mentor

Educational CLI for the Linux filesystem and Debian packages.
Designed for beginners and professionals on Debian, Ubuntu, Kali, and similar systems.

Status: InRelease CLI version.
A full conversational AI agent version is planned and will be released later.
This repository focuses on a fast, lightweight, zero-dependency educational tool.


Why fsmentor?

The Linux filesystem looks complex at first. Tools like which, whereis, and dpkg -L only show paths — they never explain why something lives in /usr/bin, /etc, or /var/lib.

fsmentor fills that gap. It gives clear, practical explanations so you always understand what you are doing.


Features:

Explain the Filesystem Hierarchy Standard (FHS) in plain language
Explain any path (/usr/bin, /etc/apt, /var/log, …)
Enhanced command lookup (which + ownership + FHS reason)
Package explanation with files grouped by purpose (binaries, configs, docs, state…)
Safe install preview that clearly states what will happen before any system change
Package search and file ownership lookup
Completely local, instant, no history storage, no external services required for this phase

Quick Start:

# Make it executable and available
sudo cp fsmentor /usr/local/bin/
sudo chmod +x /usr/local/bin/fsmentor

# Or run directly
python3 fsmentor
--------

Commands:

Command
What it does
Example
--------

fsmentor
Friendly overview + common examples
fsmentor
--------
fsmentor fhs
Full map of the Linux filesystem
fsmentor fhs
--------
fsmentor path <path>
Explain any directory or path
fsmentor path /etc
--------
fsmentor cmd <name>
Explain a command (enhanced which)
fsmentor cmd python3
--------
fsmentor pkg <name>
Explain a package + where its files live
fsmentor pkg nginx
--------
fsmentor install <name>
Clear preview + strong confirmation before install
fsmentor install openvpn
--------
fsmentor search <term>
Search packages
fsmentor search editor
--------
fsmentor owner <file>
Which package owns this file?
fsmentor owner /usr/bin/ls
--------
fsmentor why <path|cmd>
Alias for path or cmd explanation
fsmentor why /var/log
--------

Examples

fsmentor fhs
fsmentor path /usr/bin
fsmentor path /etc/apt
fsmentor cmd ls
fsmentor pkg coreutils
fsmentor install htop
fsmentor search python3
fsmentor owner /bin/bash
--------

Design Goals:
Instant – no history, no database, no background processes
Zero extra dependencies – only Python 3 + tools already on Debian systems
Educational – every answer teaches the why, not just the what
Safe – never runs destructive actions without confirmation
Contributable – clean code, easy to extend
--------

Roadmap:
Core FHS explanations
Path, command, and package explanations
Smart install preview
More system areas (services, logs, networking, systemd)
Better interactive help
Conversational AI agent version (planned – will be announced here)
Contributing
Contributions are very welcome!
Fork the repository
Create a branch (git checkout -b feature/my-improvement)
Make your changes
Test on a Debian-based system (Ubuntu / Kali recommended)
Open a Pull Request


Please keep the tool lightweight and educational.
Large language-model / always-on agent features belong in the future agent version.

License:
MIT License – see LICENSE

Author

Built to help early learners actually understand the Linux filesystem instead of just memorising commands and paths
