# Window Manager Scheme Toggler

Scripts to change the system color scheme between dark and light.

![Toggling dark scheme](https://github.com/mjkloeckner/wm-scheme-toggle/assets/64109770/55188134-b6e2-42dd-96d4-cd9058de0a5c)

## Dependencies
The basic dependencies for my use case are:

- sed
- perl
- qt5ct
- qt6ct
- gsettings
- xsettingsd
- neovim-remote
- st patched (support sending user signals to switch schemes)

This will vary from system to system, for example, if you don't use neovim and
you use a different editor or terminal, etc. In that case, you can modify the
scripts in order to fit your system.

## Quick Start

If you want to switch the color scheme just run `$ ./sys-toggle-scheme` which is
a wrapper around `sys-dark-scheme` and `sys-light-scheme`.

## Troubleshooting

As of `11 march 2024` some GTK4 apps are not following the preferred scheme due
to a problem apparently on `xdg-desktop-portal` (check out [this
discussion](https://bbs.archlinux.org/viewtopic.php?id=289408)) the solution
taken from the linked discussion is to create
`~/.config/xdg-desktop-portal/portals.conf` and add the following content

```
[preferred]
default=gtk
```

## LICENSE

[MIT](https://opensource.org/licenses/MIT)
