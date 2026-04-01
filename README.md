# [mesa-rc](https://copr.fedorainfracloud.org/coprs/adil192/mesa-rc/)

Almost-stable releases of mesa3d graphics drivers: get the newest features with the fewest bugs.

This repo is an alternative to `mesa-git` copr repos.
Instead of the bleeding edge git versions, we stick to releases and release candidates from the Mesa team.
This somewhat shields against instability from unreleased mesa versions.

Use at your own risk!

#### Install

Enable this copr repo, update your packages, and reboot:
```bash
sudo dnf copr enable adil192/mesa-rc
sudo dnf update --refresh
reboot
```

#### Uninstall

You can temporarily revert to Fedora's stable packages with this command. The next time you update your packages, mesa-rc will be reinstalled.
```bash
sudo dnf --disablerepo=copr:copr.fedorainfracloud.org:adil192/mesa-rc* distro-sync
```

Or permanently go back to Fedora's stable packages:
```bash
sudo dnf copr remove adil192/mesa-rc
sudo dnf distro-sync
```

#### Cloning

This repo is forked from Fedora's official mesa package sources.

If you want to clone this repo to contribute, run this:
```
git clone https://github.com/adil192/mesa.git
cd mesa
git remote add upstream https://src.fedoraproject.org/rpms/mesa.git
git fetch upstream main
```
