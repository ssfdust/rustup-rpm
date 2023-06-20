Rustup SPEC
-----------
The rpm spec for rustup. Convert from archlinux PKGBUILD. Most codes are generated from GTP-4.

## Build

```bash
sudo dnf install -y rpm-build rpmdevtools
sudo dnf build-dep -y rustup.spec
spectool -g -R rustup.spec
cp rustup-profile.sh ~/rpmbuild/SOURCES
rpmbuild -ba rustup.spec
```
If you use custom rust registry, you may be need to install git tool.

## Install

```bash
sudo dnf install --allowerasing -y ~/rpmbuild/RPMS/x86_64/rustup*.rpm
```
