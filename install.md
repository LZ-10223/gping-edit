Table of Contents
=================

   * [Install :cd:](#install-cd)
   * [Usage :saxophone:](#usage-saxophone)

<a href="https://repology.org/project/gping/versions">
    <img src="https://repology.org/badge/vertical-allrepos/gping.svg" alt="Packaging status" align="right">
</a>

# Install :cd:

* macOS
  * [Homebrew](https://formulae.brew.sh/formula/gping#default): `brew install gping`
  * [MacPorts](https://ports.macports.org/port/gping/): `sudo port install gping`
* Linux (Homebrew): `brew install gping`
* CentOS (and other distributions with an old glibc): Download the MUSL build from the latest release
* Windows/ARM: 
  * Scoop: `scoop install gping`
  * Chocolatey: `choco install gping`
  * Download the latest release from [the github releases page](https://github.com/orf/gping/releases)
* Fedora ([COPR](https://copr.fedorainfracloud.org/coprs/atim/gping/)): `sudo dnf copr enable atim/gping -y && sudo dnf install gping`
* Cargo (**This requires `rustc` version 1.67.0 or greater**): `cargo install gping`
* Arch Linux: `pacman -S gping`
* Alpine linux: `apk add gping`
* Ubuntu >23.10/Debian >13: `apt install gping`
* Ubuntu/Debian ([Azlux's repo](https://packages.azlux.fr/)):
```bash
echo 'deb [signed-by=/usr/share/keyrings/azlux.gpg] https://packages.azlux.fr/debian/ bookworm main' | sudo tee /etc/apt/sources.list.d/azlux.list
sudo apt install gpg
curl -s https://azlux.fr/repo.gpg.key | gpg --dearmor | sudo tee /usr/share/keyrings/azlux.gpg > /dev/null
sudo apt update
sudo apt install gping
```
* Gentoo ([dm9pZCAq overlay](https://github.com/gentoo-mirror/dm9pZCAq)):
```sh
sudo eselect repository enable dm9pZCAq
sudo emerge --sync dm9pZCAq
sudo emerge net-misc/gping::dm9pZCAq
```
* FreeBSD:
  * [pkg](https://www.freshports.org/net-mgmt/gping/): `pkg install gping`
  * [ports](https://cgit.freebsd.org/ports/tree/net-mgmt/gping) `cd /usr/ports/net-mgmt/gping; make install clean`
* Docker:
```sh
# Check all options
docker run --rm -ti --network host ghcr.io/orf/gping:gping-v1.15.1 --help
# Ping google.com
docker run --rm -ti --network host ghcr.io/orf/gping:gping-v1.15.1 google.com
```
* Flox:
```sh
# Inside of a Flox environment
flox install gping
```

