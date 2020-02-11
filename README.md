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
'SSDT-GPRW.aml' (_PRW USB wake up patch)
'SSDT-PLUG-_SB.PR00.aml' (plugin-type=1)
'SSDT-SBUS.aml' (SBUS)
'SSDT-PNLF.aml' (Notebook brightness)
'SSDT-PNLFCFL.aml' (Notebook brightness for coffeelake)
'SSDT-USBX.aml' (USB power property injection)
'SSDT-XOSI.aml' (activate Trackpad under Darwin)
'SSDT-ARTC.aml' (Apple uses ARTC instead of RTC0)
'SSDT-UIAC.aml' (Block empty usb ports)
'SSDT-TPDT.aml' (Enable GPIO for Trackpad)
'SSDT-PMC.aml' (Enable native nvram for 300-series)
## Patch
EC0 to EC: Find '4543305F' Replace '45435F5F'
