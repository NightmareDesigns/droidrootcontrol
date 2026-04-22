# droidrootcontrol

Quick reference for **USB-C phone service workflows** (firmware restore, diagnostics, and developer access) on Motorola, Samsung, and Apple devices.

## 1) USB-C to USB-C setup

- Use a **USB 3.x data cable** (not charge-only).
- If direct C-to-C is unstable, use:
  - powered USB-C hub, or
  - USB-C to USB-A adapter + known-good USB-A data cable.
- Install platform drivers/tools before connecting devices.

## 2) Core cross-platform tools

- **ADB / Fastboot** (Android platform-tools) for diagnostics, flashing, and bootloader workflows.
- **Heimdall** (Samsung, open-source Odin alternative).
- **libimobiledevice** (Apple device communication on Linux/macOS).

## 3) Vendor-specific practical options

### Motorola

- `fastboot` (official unlock-capable models, bootloader commands, flash partitions).
- **Rescue and Smart Assistant (LMSA)** for official firmware recovery.
- Official Motorola bootloader unlock portal (device-dependent).

### Samsung

- **Odin** (Windows) for official firmware packages.
- **Heimdall** (cross-platform alternative for many models).
- Download/Recovery mode + correct model-specific firmware is required.

### Apple (iPhone/iPad)

- **Finder / Apple Devices / iTunes** restore + recovery/DFU workflows.
- **idevice* tools** via libimobiledevice for diagnostics.
- Bootloader unlocking is not generally available like Android OEM unlock flows.

## 4) Important notes

- Use only firmware built for the **exact model/region/carrier variant**.
- Back up data before flashing.
- Keep battery charged and avoid cable disconnects during writes.
- Respect local laws, ownership, and anti-theft protections.
