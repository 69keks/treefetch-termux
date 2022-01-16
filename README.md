# DISCLAIMER: ALL CREDITS TO @angelofallars on github for the program. I just edited it a little so it more or less works on termux.
* To-Do: Fix get_uptime function to work with `date` command just like neofetch as `/proc/uptime` is denied from being accessed on android.

# 🌳 `treefetch`

A lightning-fast minimalist system fetch tool made in Rust. Even faster than neofetch and pfetch. Made to practice my(angelofallars') new Rust skills 🦀.

A great pair for [cbonsai](https://gitlab.com/jallbrit/cbonsai), to help you get upvotes on your Linux rice.

<img src="https://user-images.githubusercontent.com/39676098/145780007-f612ceff-7414-4bbe-af14-e2d48004ed9d.png" alt="treefetch" width=380px>

More trees with `treefetch --bonsai` and `treefetch --xmas`!

<img src="https://user-images.githubusercontent.com/39676098/149612115-2a02d617-d70a-4eed-bcce-2dd590698ea1.png" alt="treefetch bonus trees" width=380px>

# Setting up environment for treefetch to run
## Adding required files and env variables for the program to find and use
- create a file called `hostname` in `${PREFIX/etc/` and add your personal choice for hostname.
- create a file called `version` under `${PREFIX}/etc/` and add the output of `uname -r` as `Linux version <uname -r output>`
- create a file called lsb-release in `${PREFIX}/etc/` and add the following field and fill it accordingly.
`DISTRIB_DESCRIPTION=''`
(This is because termux is not FHS compliant.) Only DISTRIB_DESCRIPTION is required out of the standard fields.
- add `export USER='<your personal choice>'` to `.bashrc` or `.profile` or `.bash_profile`.

## Compiling Manually is the only way to use this currently.

To compile and install treefetch manually, you first need to install the Rust
compiler `pkg install rust`.

- `git clone https://github.com/angelofallars/treefetch`
- `cd treefetch`
- `cargo install --path .`
- Add `export PATH="/data/data/com.termux/files/home/.cargo/bin:$PATH"` to `.bashrc` and run `. ~/.bashrc` in-case the dir is not in your termux's `$PATH`

## Usage

```
Usage:
  treefetch [options]

OPTIONS
  -b, --bonsai   Show a bonsai tree
  -x, --xmas     Show a Christmas tree
  -h, --help     Display this help message
```

## Contributing

Just make sure to develop and make pull requests on the `dev` branch instead of
the `main` branch.

**Contribute to treefetch and get your awesome profile picture displayed here!**

<a href="https://github.com/angelofallars/treefetch/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=angelofallars/treefetch" />
</a>

*Made with [contrib.rocks](https://contrib.rocks).*

## Supporting this project

This project is free and open-source and will always be that way.

If you like this project, please consider donating to angelofallars on github to improve this project even further.

<a href="https://www.buymeacoffee.com/angelofallaria" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/default-orange.png" alt="Buy Me A Coffee" width="140"></a>

## License

This program is licensed under the GPLv3 License.
