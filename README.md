# Arch Chroot Utilities
A collection of scripts that make it simple to setup, enter, and delete an Arch Linux chroot. Requires an Arch Linux host system.

# Obtaining
You can download the latest main branch on GitLab as a compressed archive ([zip](https://gitlab.com/nickgirga/acu/-/archive/main/acu-main.zip)|[tag.gz](https://gitlab.com/nickgirga/acu/-/archive/main/acu-main.tar.gz)|[tar.bz2](https://gitlab.com/nickgirga/acu/-/archive/main/acu-main.tar.bz2)|[tar](https://gitlab.com/nickgirga/acu/-/archive/main/acu-main.tar)) or you can find versioned releases as compressed archives on the [releases](https://gitlab.com/nickgirga/acu/-/releases) page. If you plan on using the main branch, I personally would recommend just using git to clone the repository: `git clone https://gitlab.com/nickgirga/acu.git arch-chroot-utilities`.

If you downloaded a compressed archive, decompress it with the appropriate utility (unzip, tar) and head to the [Usage](#usage) section.

# Usage
First, [obtain](#obtaining) the scripts. These scripts require no installation. The creation and starting scripts require two packages and you probably already have one installed: `util-linux` and `devtools`. However, they will automatically be installed if they are needed.

All you have to do do get an Arch Linux chroot up and running is nativate to the repository's root directory and run `./create-chroot` (wait for it to complete) and run `./start-chroot` to enter it. If you need to destroy it, simply run `./delete-chroot`. The utilities that comes with `devtools` will take care of many things such as networking, copying mirrorlists, etc. The Arch Chroot Utilities you find in this repository will take care of things such as mounting/unmounting, ensuring the user doesn't do anything too dangerous (like deleting the filesystem while it's mounted), and installing needed dependencies. It also just makes it much easier to type. This last point can be especially appreciated when creating and destroying the same container over and over again.

Note that these scripts were created for the convenience of developers for internal use and are not intended to be used in other contexts. Regardless of the context of your use, it would be wise to look over the scripts yourself before running them. They aren't complex at all because they utilize a few other chroot utilities from the `devtools` package.
