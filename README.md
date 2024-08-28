# zmk-config

## Keymap

This is a [ZMK](https://zmk.dev) config repo for my ergonomic keyboards.
The keymap is optimized to be usable with 28-30 keys, with dropped keys from inner index and pinky columns and one or two thumb keys each, like the [Hummingbird](https://github.com/PJE66/hummingbird) layout.
Currently these keyboards are:
- A hand-wired [Rommana](https://github.com/AlaaSaadAbdo/Rommana) (30 keys)
- A [Rufous](https://github.com/jcmkk3/trochilidae#rufous) (30 keys)
- A hand-wired, modified [Grumpy](https://github.com/caksoylar/Grumpy/tree/hummingbird-pinky) (28 keys)
- [Corne-ish Zen](https://lowprokb.ca/products/corne-ish-zen) (36 keys)

It mainly uses three non-base layers activated through two thumb keys, along with combos. It has <kbd>Ctrl</kbd>/<kbd>Shift</kbd> thumb hold-taps along with home row mods, which are also available on the left side of `NAV` layer.
`FUN` layer is implemented as a tri-layer, i.e. it is active when both `NAV` and `SYM` are active.

The default alpha layer is a modification of Colemak-DH and an alternative is the [Bird layout](https://github.com/jcmkk3/bird-layout).

OS-dependent shortcuts are present on the `NAV` and `FUN` layers, e.g. for Windows:
- `Win Close`: <kbd>Alt</kbd><kbd>F4</kbdy>
- `Tab Next`: <kbd>Ctrl</kbd><kbd>Tab</kbd>
- `Tab Prev`: <kbd>Ctrl</kbd><kbd>Shift</kbd><kbd>Tab</kbd>
- `Tab Close`: <kbd>Ctrl</kbd><kbd>F4</kbd>
- `Desk Next`: <kbd>Ctrl</kbd><kbd>Gui</kbd><kbd>Right</kbd>
- `Desk Prev`: <kbd>Ctrl</kbd><kbd>Gui</kbd><kbd>Left</kbd>
- `Win Next`: <kbd>Alt</kbd><kbd>Tab</kbd> (hold Alt while layer active) using [swapper](#zmk-customizations)
- `Win Prev`: <kbd>Alt</kbd><kbd>Shift</kbd><kbd>Tab</kbd> (hold Alt while layer active)

Below representation was generated with [`keymap-drawer`](https://github.com/caksoylar/keymap-drawer) using the [automated Github workflow](https://github.com/caksoylar/keymap-drawer/tree/main#setting-up-an-automated-drawing-workflow)
-- check out the drawings for all keyboards in the [`keymap-drawer` folder](keymap-drawer/).

![Keymap Representation](./keymap-drawer/hummingbird.svg?raw=true "Keymap Representation")

See my [QMK userspace](https://github.com/caksoylar/qmk_userspace/) for equivalent keymap definitions for QMK, although note that they might not be up-to-date with latest QMK changes.

## LED indicators widget

Some keyboards in this repo include an indicator widget utilizing an RGB LED, like the user LEDs on a Xiao BLE.
This widget is a ZMK module housed in [`zmk-rgbled-widget`](https://github.com/caksoylar/zmk-rgbled-widget) -- check out the repo and the instructions to use it with your keyboards!

## ZMK customizations

I use a custom ZMK branch referenced in [west.yml](config/west.yml) which contains a few extras, namely [mouse keys](https://github.com/zmkfirmware/zmk/pull/2027) used in the `MSE` layer and [display improvements for the Corne-ish Zen](https://gist.github.com/caksoylar/c411313990978e1903c244f03039187a).
For a variant of my configuration tailored for stock ZMK, check out the [`stock` branch](https://github.com/caksoylar/zmk-config/tree/stock).

It also uses a swapper key for single button window switching, defined using [the tri-state behavior module](https://github.com/caksoylar/zmk-tri-state).
