## ⚙️ sysctl hardening

#### Usage:

- Clone the repository in `~/Downloads`
```
$ cd ~/Downloads && git clone --depth 1 https://github.com/g5ostXa/sysctl.git
```
- Copy sysctl files to `/etc/sysctl.d/` (Note that you might need to create the directory first)
```
$ sudo mkdir /etc/sysctl.d/; sudo cp -r "$HOME"/Downloads/sysctl/* /etc/sysctl.d/
```
- Give root permissions to the directory and all it's content
```
$ sudo chown -R root:root /etc/sysctl.d/; sudo chown -R root:root /etc/sysctl.d/*
```
- Remove `README.md`, `sysctl` directory and `LICENSE` if not needed
```
$ sudo rm -rf /etc/sysctl.d/README.md; sudo rm -rf /etc/sysctl.d/LICENSE; rm -rf ~/Downloads/sysctl/
```
- Apply kernel parameters
```
$ sudo sysctl --system
```

