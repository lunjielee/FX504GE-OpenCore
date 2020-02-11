# FX504GE-OpenCore
- macOS Catalina 10.15.4 Beta
- Bios FX504GE.318
# Hardware Specs
- CPU: Intel Core i7-8750H 6 cores, 12 threads
- GPU: Intel UHD Graphics 630 + nVidia GTX 1050Ti Mobile(Blocked)
- RAM: 16GB(8+8)
- Audio: ALC255(layout 3)
- Trackpad: ELAN1200
- WD Black SN720 500GB NVMe SSD Gen3.0x4
- Intel Wireless-AC 9560(Replaced With DW1820A)
# What's working
- Intel UHD Graphics 630
- WiFi & Bluetooth
- Audio
- Backlight Control (PS2 key remapping or [Karabiner-Elements](https://pqrs.org/osx/karabiner/))
- Ethernet
- Trackpad
- USB
- Camera
# What's not working
- nVidia GTX 1050Ti Mobile


# Before Installation
- Secure Boot: Disabled
- SATA mode: AHCI
- DVMT-Preallocated: 64MB
# ACPI
## Add
1. `SSDT-GPRW.aml` (_PRW USB wake up patch)
2. `SSDT-PLUG-_SB.PR00.aml` (plugin-type=1)
3. `SSDT-SBUS.aml` (SBUS)
4. `SSDT-PNLF.aml` (Notebook brightness)
5. `SSDT-PNLFCFL.aml` (Notebook brightness for coffeelake)
6. `SSDT-USBX.aml` (USB power property injection)
7. `SSDT-XOSI.aml` (activate Trackpad under Darwin)
8. `SSDT-ARTC.aml` (Apple uses ARTC instead of RTC0)
9. `SSDT-UIAC.aml` (Block empty usb ports)
10. `SSDT-TPDT.aml` (Enable GPIO for Trackpad)
11. `SSDT-PMC.aml` (Enable native nvram for 300-series)
## Patch
1. EC0 to EC: Find `4543305F` Replace `45435F5F`
