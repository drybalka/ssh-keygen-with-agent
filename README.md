# ssh-keygen-with-agent

If you are using SSH for signing Git commits then you may be forced to enter your password each time.
This is because by default the signing `ssh-keygen` command does not add keys to `ssh-agent`.
This simple wrapper script solves this problem by automatically adding SSH keys to the agent when signing Git commits.

## Installation

Copy the script to a directory in your PATH and make it executable, for example:

```bash
sudo cp ssh-keygen-with-agent /usr/local/bin/
sudo chmod +x /usr/local/bin/ssh-keygen-with-agent
```

Arch Linux users may instead build and install from the PKGBUILD:

```bash
makepkg --clean --install && rm *.pkg.tar.zst
```

## Usage

Configure Git to use this script for SSH commit signing:

```bash
git config --global gpg.ssh.program ssh-keygen-with-agent
```
