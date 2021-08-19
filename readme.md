# SB ENERGY MANAGEMENT
A full automated energy management script for Starbase

## Guilded Server (better than Discord)

You can join me on Guilded for help or suggestions or requests by following that link : https://guilded.jericho1060.com

### Modes

This system will give you 4 modes for you energy system

- Shutdown: it will stop your power
- Auto: it will adjust the power elevel depending on your batteries and can save fuel
- Half: Force the power to 50%
- Override: Force the power to 100%

### Elements required

- 6 `Basic YOLOL chips` (you can only use 3 but the performance will be slower)
- 1 `Text panel 24x24`
- 2 `Simple buttons 12x12`
- 1 `YOLOL memery chip`
- 7 `YOLOL chip sockets` or 3 `YOLOL Racks 48x48` with 1 `YOLOL Rack chip slot(2 slots)` and 2 `YOLOL Rack chip slot (3 Slots)`

### Example for Mounting the display and buttons

### Example for Mounting the Script Racks

### The buttons

#### Top Button Fields


#### Bottom Button fields


### Text Panel


### Memory chip

On the memory chip, just replace the 1st field with the name `GenModeNb` and set it to `4` (this is the value for auto power)

### Scripts

If you are using 6 you can copy each of the folowing files on a single basic chip and plug them:

- `main.yolol` will manage the fuel chmaber rate depending on th emode you selected
- `screen.yolol` will manage the display on the text panel
- `button1.yolol` will manage the press on the bottom button
- `button2.yolol` will manage the press on the top button
- `higher_limit.yolol` will reset the value of `GenModeNB` to shutdown if it goes higher than the overide
- `higher_limit.yolol` will reset the value of `GenModeNB` to override if it goes lower than the shutdown

if you are only using 3 chips, you only need these 3 scripts : `main.yolol`, `screen.yolol`, `buttons_group.yolol`.
The third one will regroupe the 4 that are managing the button states and the limits.
