# Home Power Monitor Hardware

[![MegaLinter](https://github.com/ScottGibb/Home-Power-Monitor-Hardware/actions/workflows/mega-linter.yaml/badge.svg)](https://github.com/ScottGibb/Home-Power-Monitor-Hardware/actions/workflows/mega-linter.yaml)
[![KiCad](https://github.com/ScottGibb/Home-Power-Monitor-Hardware/actions/workflows/kicad.yaml/badge.svg)](https://github.com/ScottGibb/Home-Power-Monitor-Hardware/actions/workflows/kicad.yaml)
[![Release Please](https://github.com/ScottGibb/Home-Power-Monitor-Hardware/actions/workflows/release-please.yaml/badge.svg)](https://github.com/ScottGibb/Home-Power-Monitor-Hardware/actions/workflows/release-please.yaml)

TODO: Picture of Final Hardware Goes Here

## Summary

This repository contains the KiCad hardware designs for the [Home Power Monitor project](https://github.com/ScottGibb/Home-Power-Monitor). It currently consists of two hardware components:

- An LCD Control Unit
- An Isolated Conversion Board between the Host Processor and the JSY-MK-194 Power Sensor

## Components

### LCD Control Unit

The `lcd_control_unit` project is the control board for the display section of the power monitor. The schematic is built around a `WC1602A` 16x2 character LCD and is designed as a board for the display assembly. The unit contains the screen along with four button inputs, one of which is connected to a PIR sensor, specifically the AM312 Mini PIR Sensor.

### Power Monitor Protection

The `power_monitor_protection` project is the interface and protection board. It includes isolation circuitry for both serial communication and power.

### External Libraries

The [libraries](./libraries/) directory contains external footprints and symbols for the project.

## Working With the Designs

Open either KiCad project directly in KiCad:

- `./lcd_control_unit/lcd_control_unit.kicad_pro`
- `./power_monitor_protection/power_monitor_protection.kicad_pro`

The custom library content used by the protection board is stored in `./libraries/`.

## Automation

GitHub Actions are configured to help keep the hardware projects consistent:

- **KiCad** runs project automation and publishes generated artifacts such as schematics, ERC reports, and BOM outputs.
- **MegaLinter** checks repository quality and formatting.
- **Release Please** prepares releases and uploads generated KiCad assets for tagged versions.
- **Dependabot Auto Merge** keeps GitHub Actions and dependency updates moving automatically.

## 3D Printed Cases and Printed Circuit Boards

Due to funding, PCB layouts were never produced for these schematics. This was largely because the boards themselves were too simple to justify manufacturing, so veroboard was used instead. 3D-printed cases were produced, however, and can be found on Printables and Thingiverse.

- TODO: Thingiverse Link
- TODO: Printables Link

## Useful Links

- [Home Power Monitor Software Repository](https://github.com/ScottGibb/Home-Power-Monitor)
- [KiCad](https://www.kicad.org/)
