<!---

This file is used to generate your project datasheet. Please fill in the information below and delete any unused
sections.

You can also include images in this folder and reference them in the markdown. Each image must be less than
512 kb in size, and the combined size of all images must be less than 1 MB.
-->
## How it works

This project is a 4-bit decade counter that stores the current count in a 4-bit register `q`. When the active-low reset pin `rst_n` is low or `q` reaches 9, the counter resets to 0; otherwise, it increments by 1 on every rising edge of `clk` and outputs the binary value on `uo_out[3:0]`.

## How to test

Pulse `rst_n` low to reset the counter output `uo_out[3:0]` to 0, then bring `rst_n` high and apply clock pulses on `clk`. Verify that `uo_out[3:0]` increments from 0 up to 9 on each rising clock edge and wraps back to 0 on the next tick.

## External hardware

No external hardware is required; the 4-bit count can be read directly from output pins `uo` through `uo`.
