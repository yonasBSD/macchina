# Macchina

![Macchina preview image](screenshots/preview.png)

![madewith](https://img.shields.io/static/v1?label=MADE%20WITH&message=RUST&color=ef4041&style=for-the-badge)
![reposize](https://img.shields.io/github/repo-size/grtcdr/macchina?color=BEE5BF&logo=github&style=for-the-badge)
![loc](https://img.shields.io/tokei/lines/github/grtcdr/macchina?color=FFD1BA&label=Lines%20of%20Code&logo=rust&style=for-the-badge)

---

# About Macchina
Macchina is a fetching program, not a library. But you can use the 
functions it relies on to extract system data in your own program.

It lets you view basic system information, like your hostname, your kernel version, memory usage, and much more.
No one wants a slow fetcher, and macchina's main goal is to provide you with handy features while keeping performance a priority.

If Macchina fails to display certain elements, or their output is incorrect, please create an [issue](https://github.com/grtcdr/macchina/issues/new).

---

# Benchmarks
Macchina is pretty fast, see for yourself:

- Execution time is measured using [hyperfine](https://github.com/sharkdp/hyperfine)

| Command | Mean [ms] | Min [ms] | Max [ms] | Relative |
|:---|---:|---:|---:|---:|
| `macchina` | 22.2 ± 0.7 | 21.0 | 25.1 | 1.00 |
| `neofetch` | 243.9 ± 2.3 | 240.0 | 246.9 | 11.01 ± 0.37 |

__Summary__: `macchina` runs __11.01 ± 0.37__ times __faster__ than `neofetch`

- Note that hiding elements using Macchina's __--hide <element>__ significantly improves speed

---

# Features
## Macchina displays basic system information such as:
- Hostname
- Product
  - Manufacturer
  - Model name
- Distribution
- Desktop Environment
- Kernel version
- Package count
- Shell
- Terminal
- Processor
  - Model name
  - Frequency
  - Thread count
- Uptime
- Memory
  - Used / Total
- Battery
  - Percentage
  - Status
- Palette

> Package count: __Pacman only__, as it will print __0__ for distributions that use any other package manager. Support for other package managers is on its way.

## Macchina supports the following arguments

`--no-color / -n` - Disable colors

`--color / -c <color>` - Specify the key color

`--separator-color / -C <color>` - Specify the separator color

`--random-color / -r` - Let Macchina pick a random color for you

`--palette / -p` - Display palette

`--short-sh / -s` - Shorten shell output (/bin/zsh -> zsh)

`--hide / -H <element>` - Hide elements such as host, os, kern, etc.

`--bar / -b` - Display memory usage and battery percentage as bars

![Preview of bar argument](screenshots/bars.png)

`--theme / -t <theme_name>` - Specify the theme

`--padding / -P <amount>` - Specify the amount of (left) padding to use

`--help / -h` -  Display help menu

`--version / -v` - Print version

---

# Installation
Macchina is available on:

- [AUR](https://aur.archlinux.org/packages/macchina/)

  Install using your favorite AUR helper or by running:
  ```
  git clone https://aur.archlinux.org/macchina.git
  cd macchina
  makepkg -si
  ```
- [crates.io](https://crates.io/crates/macchina)

  Install using cargo:
  ```
  cargo install macchina
  ```
  
---

# Platform Support

|  Platform     |      Support       |
| :-:           |        :-:         |
| Linux         |         X          |
| BSD           |         ?          |
| MacOS         |                    |
| Windows       |                    |

Cells containing X: Macchina supports that platform

Cells containing ?: Macchina has not been tested yet on that platform

Empty cells: Macchina does not support that platform