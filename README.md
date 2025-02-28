# Glitch Tag Zephyr Support

This repo is a simple board description that allows builds of [Zephyr RTOS](https://www.zephyrproject.org) targeting the [hextree.io](hextree.io) Glitch Tag device.

## Usage

To use this board description, point your `BOARD_ROOT` cmake variable to this repo, and the `glitch_tag` board should be usable within Zephyr's ecosystem.

From within a west virtual environment at the zephyr project root, run

```
west build -p -b glitch_tag samples/basic/blinky -- -DBOARD_ROOT=/path/to/this/repo
```
to build the basic blinky sample for the Glitch Tag.

## Supported Interfaces

The Glitch Tag is a simple board, and this port supports

* The two LEDs on the board via `led0` and `led1` devicetree entries.
* UART output through usual Zephyr driver interfaces

## Why?

I wanted an easy way to experiment with glitch attacks with my own code running on the Glitch Tag.
