# SB ENERGY MANAGEMENT

A full automated energy management script for Starbase.

Showcase Video: https://youtu.be/u-j5BeoDx4c

## Guilded Server (better than Discord)

You can join me on Guilded for help or suggestions or requests by following that link : https://guilded.jericho1060.com

## Modes

This system will give you 4 modes for you energy system

- Shutdown: it will stop your power
- Auto: it will adjust the power elevel depending on your batteries and can save fuel
- Half: Force the power to 50%
- Override: Force the power to 100%

## Elements required

- 6 `Basic YOLOL chips` (you can only use 3 but the performance will be slower)
- 1 `Text panel 24x24`
- 2 `Simple buttons 12x12`
- 1 `YOLOL memery chip`
- 7 `YOLOL chip sockets` or 3 `YOLOL Racks 48x48` with 1 `YOLOL Rack chip slot(2 slots)` and 2 `YOLOL Rack chip slot (3 Slots)`

## Example for Mounting the display and buttons

![Mounting](https://github.com/Jericho1060/sb-energy-management/blob/main/pictures/DisplayButtonsMounting.jpg?raw=true)

## Example for Mounting the Script Racks

![Mounting](https://github.com/Jericho1060/sb-energy-management/blob/main/pictures/RackMounting.jpg?raw=true)

## Fuel Chamber and Generators

Do not change anything on genetors, you can keep the rate to 100% it will not affect how much fuel you are using.

If the generator is set at 100% and the fuel chamber is at 10%, the generator will auto adjust to use what the chamber are giving.

If a generator is set at 10% but the chamber is set at 100%, this will still fully use you fuel rod, the more you are producing is just lost.

So alway let your generators to 100% and only adjust your chamber.

### Generator (default fields)

![Generators fields](https://github.com/Jericho1060/sb-energy-management/blob/main/pictures/Generator.jpg?raw=true)

### Fuel Chamber (default fields)

![Chamber fields](https://github.com/Jericho1060/sb-energy-management/blob/main/pictures/FuelChamber.jpg?raw=true)

## The buttons

### Top Button Fields

![Button fields](https://github.com/Jericho1060/sb-energy-management/blob/main/pictures/ButtonTop.jpg?raw=true)

### Bottom Button fields

![Button fields](https://github.com/Jericho1060/sb-energy-management/blob/main/pictures/ButtonBottom.jpg?raw=true)

## Text Panel

![Text Panel fields](https://github.com/Jericho1060/sb-energy-management/blob/main/pictures/TextPanel.jpg?raw=true)


## Memory chip

On the memory chip, just replace the 1st field with the name `GenModeNb` and set it to `4` (this is the value for auto power)

![Memory Chip fields](https://github.com/Jericho1060/sb-energy-management/blob/main/pictures/MemoryChip.jpg?raw=true)

## Scripts

If you are using 6 you can copy each of the folowing files on a single basic chip and plug them:

- `main.yolol` will manage the fuel chmaber rate depending on th emode you selected
- `screen.yolol` will manage the display on the text panel
- `button1.yolol` will manage the press on the bottom button
- `button2.yolol` will manage the press on the top button
- `higher_limit.yolol` will reset the value of `GenModeNB` to shutdown if it goes higher than the overide
- `higher_limit.yolol` will reset the value of `GenModeNB` to override if it goes lower than the shutdown

if you are only using 3 chips, you only need these 3 scripts : `main.yolol`, `screen.yolol`, `buttons_group.yolol`.
The third one will regroupe the 4 that are managing the button states and the limits.

## Support or donation

if you like it, [<img src="https://github.com/Jericho1060/DU-Industry-HUD/blob/main/ressources/images/ko-fi.png?raw=true" width="150">](https://ko-fi.com/jericho1060)