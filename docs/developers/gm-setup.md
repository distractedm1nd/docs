---
sidebar_label: Setup
---

# 💻 Setup

- Operating systems: GNU/Linux, macOS, or Windows Subsystem for Linux (WSL).
Recommended GNU/Linux or macOS.

- [Golang](https://go.dev)
- [Ignite CLI v0.25.1](https://github.com/ignite/cli)
- [Homebrew](https://brew.sh)
- [wget](https://www.gnu.org/software/wget)
- [jq](https://stedolan.github.io/jq)
- [A Celestia Light Node](/nodes/light-node.mdx)

## 🏃 Install Golang

Celestia-App, Celestia-Node, and Cosmos-SDK are written in the Golang
programming language. You will need Golang to build and run them.
> **Be sure to use the same testnet installation instructions through this
entire tutorial**

You can [install Golang here](../nodes/environment.mdx#install-golang).

## 🔥 Install Ignite CLI

First, you will need to create `/usr/local/bin` if you have not already:

```bash
sudo mkdir -p -m 775 /usr/local/bin
```

Run this command in your terminal to install Ignite CLI:

```bash
curl https://get.ignite.com/cli! | bash
```

> ✋ On some machines, you may run into permissions errors like the one below.
You can resolve this error by following the guidance
[here](https://docs.ignite.com/guide/install#write-permission) or below.

```bash
# Error
jcs @ ~ % curl https://get.ignite.com/cli! | bash


  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  3967    0  3967    0     0  16847      0 --:--:-- --:--:-- --:--:-- 17475
Installing ignite v0.25.1.....
######################################################################## 100.0%
mv: rename ./ignite to /usr/local/bin/ignite: Permission denied
============
Error: mv failed
```

The following command will resolve the permissions error:

```bash
sudo curl https://get.ignite.com/cli! | sudo bash
```

A successful installation will return something similar the response below:

```bash
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  3967    0  3967    0     0  15586      0 --:--:-- --:--:-- --:--:-- 15931
Installing ignite v0.25.1.....
######################################################################## 100.0%
Installed at /usr/local/bin/ignite
```

Verify you’ve installed Ignite CLI by running:

```bash
ignite version
```

The response that you receive should look something like this:

<!-- markdownlint-disable MD013 -->
```bash
jcs @ ~ % ignite version
Ignite CLI version: v0.25.1
Ignite CLI build date: 2022-10-20T15:52:00Z
Ignite CLI source hash: cc393a9b59a8792b256432fafb472e5ac0738f7c
Cosmos SDK version: v0.46.3
Your OS: darwin
Your arch: arm64
Your Node.js version: v18.10.0
Your go version: go version go1.19.2 darwin/arm64
Your uname -a: Darwin Joshs-MacBook-Air.local 21.6.0 Darwin Kernel Version 21.6.0: Mon Aug 22 20:20:07 PDT 2022; root:xnu-8020.140.49~2/RELEASE_ARM64_T8110 arm64
Your cwd: /Users/joshstein
Is on Gitpod: false
```
<!-- markdownlint-enable MD013 -->

## 🍺 Install Homebrew

Homebrew will allow us to install dependencies for our Mac:

```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Be sure to run the commands similar to the output below from the successful installation:

```sh
==> Next steps:
- Run these three commands in your terminal to add Homebrew to your PATH:
    echo '# Set PATH, MANPATH, etc., for Homebrew.' >> /Users/joshstein/.zprofile
    echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/joshstein/.zprofile
    eval "$(/opt/homebrew/bin/brew shellenv)"
```

## 🏃 Install wget and jq

wget is an Internet file retriever and jq is a lightweight and flexible
command-line JSON processor.

```bash
brew install wget && brew install jq
```
