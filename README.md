# dwm
## my version of dwm

## Information

### Patches:
- [`dwm-autostart`](https://dwm.suckless.org/patches/autostart/): run `~/.dwm/autostart.sh` and `~/.dwm/autostart_blocking.sh` on startup
- [`dwm-centeredmaster`](https://dwm.suckless.org/patches/centeredmaster): the centered master layout
- [`dwm-fullgaps`](https://dwm.suckless.org/patches/fullgaps): add gaps to the tile layout
- [`dwm-rotatestack`](https://dwm.suckless.org/patches/rotatestack): allow for rotating windows on the stack
- [`dwm-systray`](https://dwm.suckless.org/patches/systray): add a systray to the bar (disabled)

### Colors
My version of dwm uses my turn on the [nightfall colorscheme](https://github.com/nghtfall).

### Autostart
My autostart is not included (due to it depending on things you might have not set) but it starts the following programs:
- `picom`: compositor for transparency, blur and shadows
- `nextcloud`: cloud synchronisation
- `nitrogen`: wallpaper setting utility
- `flameshot`: screenshot utility (launches into systray)
- `dwmbar`: a script on my machine for setting the bar

### Bar
My bar displays the following things:
- time
- weather
- disk space free (on root partition)

As a separator I use the pipe character (`|`).

For your own bar you use the `xsetroot` command.
For example `xsetroot -name 'I love dwm'` sets the bar to 'I love dwm' (not the entire bar only a specific part of the bar that's on the right in this configuration).
You can also use things like the time and date to be displayed in the bar: `xsetroot -name "$(date)"`
To let it update you can put it in a while loop: `while :; xsetroot -name "$(date)"; sleep 1; done`.
Then you can add that to the `autostart.sh` file like this:
```bash
while :; xsetroot -name "$(date)"; sleep 1; done &
```

### Fonts
My configuration uses the mononoki Font

## Installation
To install my version of dwm clone the repository and run `make clean install` as root.
Per default dwm will be installed to `/usr/local/bin/dwm`. To change that edit the `config.mk` file.

