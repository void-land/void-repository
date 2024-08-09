# Void Linux Packages Repository
This repository contains packages for various applications and libraries built for Void Linux.

Available Packages
The repository currently provides binary packages for the following architectures:

- x86_64-glibc

Adding the Repository
To add this repository to your Void Linux system, create a new file (e.g., `/etc/xbps.d/void-repository.conf`) with the following content:

```
echo 'repository=https://raw.githubusercontent.com/void-land/void-repository/repository-x86_64-glibc' | sudo tee /etc/xbps.d/void-repository.conf
```

```
echo 'repository=https://github.com/void-land/void-repository/releases/latest/download/' | sudo tee /etc/xbps.d/void-repos.conf
```

Replace `repository-x86_64-glibc` with the appropriate branch name for your desired architecture (e.g., `repository-x86_64-musl` for the musl libc variant).

Installing Packages
Once you've added the repository, you have to sync the repo :

```
sudo xbps-install -S
```

You can also search for available packages using `xbps-query`:

```
xbps-query -Rs google-chrome
```
