# Arch Repo

Experimental custom Arch Linux package repository leveraging automated workflow-based builds.

## Using Repo

```shell
curl https://raw.githubusercontent.com/bgh-github/arch-repo/main/public-key.asc | sudo pacman-key --add -
sudo pacman-key --lsign-key bgh

sudo sed --in-place --expression='\@^\[core\]$@i [custom-bgh]\nSigLevel = Required\nServer = https://repo.bgh.io/arch/$repo/os/$arch\n' /etc/pacman.conf
```
