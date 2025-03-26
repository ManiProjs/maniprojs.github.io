---
layout: single
---

Cakeman is a no-nonsense C and C++ package manager.

In this article, I want to talk about Cakeman.

It is built by me, and avaliable in [BeagleSoftware](https://github.com/beaglesoftware/cakeman)'s [GitHub organization](https://github.com/BeagleSoftware).

## About Cakeman

Cakeman is a command-line tool that allows you to manage headers for your C/C++ projects without any disasters, and is designed to be fast and efficient.

It is written in Go, which means it is fast and efficient. It is also easy to use and has a simple interface.

## Features

Cakeman has the following features:

- Fast and efficient
- Easy to use
- Simple interface
- Lightweight
- Cross-platform (not tested on Windows and Linux)

## How it works

Currently, Cakeman is not avaliable for everyone and installation guide is not avaliable.

However, you can build it from source.

#### Requirements
- [Go](https://golang.org/dl/).
- Internet connection
- [Git](https://git-scm.com/downloads)
- A C/C++ compiler [(1)](#which-compiler-is-suitable-for-your-system)

### Build from source
This process is automated. Unfortunately, the script is not ready yet.

Alternatively, You can do it manually.

```zsh
# Clone the repository
git clone https://github.com/maniprojs/cakeman.git && cd cakeman

export OS_1=$(uname -s)

if [ $OS_1 = "Darwin" ]; then
    export OS="macos"
elif [ $OS_1 = "Linux" ]; then
    export OS="linux"
fi

export ARCH=$(uname -m)

# Build it
./build.sh
# Binaries are ready to use.
./dist/$OS/$ARCH/cakeman
```

# License
Cakeman is licensed with MIT License.

You can:
- Use the source code
- Modify the source code
- Distribute Cakeman
- Commercial use

You can't:
- Put a warranty
- Liability
- Support

Read the [LICENSE](https://github.com/beaglesoftware/cakeman/blob/master/LICENSE) for more information.

###### Which compiler is suitable for your system?
###### If you use a Mac, Clang is the compiler you should use. It is included in Xcode Developer Command-Line Tools. (You just need command-line tools, Xcode is not required)
###### Install it with this command: `xcode-select --install`
###### If you use Linux, GCC and G++ is the compiler you should use. Install it using your package manager.
###### Debian-based distros (e.g. Ubuntu, Debian, Linux Mint, etc.) (Using APT): `sudo apt install build-essential`
###### Fedora-based distros (e.g. Fedora, CentOS, RHEL, etc.) (Using DNF): `sudo dnf install gcc gcc-c++ make`
###### Arch-based distros (e.g. Arch Linux, Manjaro, etc.) (Using Pacman): `sudo pacman -S gcc gcc-libs g++ make`
