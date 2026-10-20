# Wiring Harnesses

WireViz sources are grouped by board:

- [pi-overview.yaml](./pi-overview.yaml): shared Raspberry Pi 2x20 header connections.
- [lcd_control_unit/](./lcd_control_unit/): buttons, PIR and contrast potentiometer.
- [power_monitor_protection/](./power_monitor_protection/): isolated meter connection.

All JST connectors use 2.54mm pitch.

## Render

From the repository root:

```sh
nix run .#render-wiring
```

HTML, PNG, SVG and TSV BOMs are generated under ignored `wiring/output/`,
matching the source folders. Wiring releases attach these outputs and sources
as `wiring.zip`.

Keep isolation-board GND1 and GND2 separate. The Pi header is shown from the
component side, with pin 1 at the top left. GPIO mappings follow the
[PiHall configuration](https://github.com/ScottGibb/Home-Lab-Containers/blob/main/PiHall/IOT/docker-compose.yml);
board contacts follow the saved KiCad schematics.
