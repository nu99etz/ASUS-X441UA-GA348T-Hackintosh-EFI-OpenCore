# ASUS X441UA-GA348T EFI Opencore Hackintosh

**Don't try this EFI in different ASUS model !!!** (Only ASUS X441UA-GA348T) **Do With Your Own Risk !!!**
**Maybe You Can Try On Same ASUS Model With ASUS Type X441UA**
**Only UEFI BIOS**
**Only SSD or HDD Formatted To GPT Scheme**
**Note : Only OpenCore v0.7.0**

============================================================================
### ASUS X441UA-GA348T 

| Laptop Type | Bios Version | Installed macOS | Bootloader |
| ----------- | ----------- | ----------- | ----------- | 
| ASUS X441UA-GA348T | ASUS Ez Mode American Megatrends V 317 | Catalina 10.15.7 | [OpenCore v0.7.0](https://github.com/acidanthera/OpenCorePkg/releases) |

### My Specifications :

| Type | Spec | Status |
| ----------- | ----------- | ----------- |
| Processor | Intel Core i3 7100U Kabylake | Working |
| Chipset | Intel Kabylake-U | Working |
| RAM | 4GB DDR4 Onboard PC 17000 (2133 Mhz) + 8GB DDR4 Corsair PC 17000 (2133 Mhz) | Working |
| IGPU | Intel HD Graphics 620 | Working |
| Storage | 1x Seagate HDD 500GB + 1x Samsung EVO 870 SSD SATA 500GB | Working |
| Wifi | Qualcomm Atheros AR956x + Bluetooth | Working But Indicator Still One Bar Overall Its Better For Me|
| Ethernet | Realtek FE PCIe Family Ethernet | Working |
| Touchpad | Asus Precision Touchpad I2CHID Interface | Working |
| Keyboard | PS/2 Interface | Working |
| Sound | Realtek ALC255, Layout ID=66 | Working |
| Battery | Battery 3 Cells 36 Whrs Battery  | Untested Because My Battery Is Broken |
| Webcam | USB2.0 VGA UVC WebCam | Working |
| SD Card Reader | Realtek Multi-Card Reader | Untested |

### System Status :

| Type | Status |
| ----------- | ----------- |
| QE/CI Graphics Intel HD 620 | Working |
| CPU Power Management | Working |
| Restart and Shutdown | Working |
| Sleep | Untested |
| Brightness Slider & FN keys F5 - F6 | Working |
| Battery Precentage | Working But My Battery Is Broken|
| Touchpad and Gesture | Working |
| HDMI Display | Working |
| HDMI Audio | Working |
| iService | Untested |

### Used Kext :

| Kext | Info |
| ----------- | ----------- |
| [Lilu.kext](https://github.com/acidanthera/Lilu/releases) | Kernel extension Arbitrary kext and process patching on macOS |
| [WhateverGreen.kext](https://github.com/acidanthera/WhateverGreen/releases) | To disable Nvidia discrete GPU and patch framebuffer Intel HD 620 |
| [AppleALC.kext](https://github.com/acidanthera/AppleALC/releases) | To patch on-board sound controllers|
| [VirtualSMC.kext](https://github.com/acidanthera/VirtualSMC/releases) | SMC Emulator Layer |
| [SMCProcessor.kext](https://github.com/acidanthera/VirtualSMC/releases) | VirtualSMC Plugin for Processor Monitoring |
| [SMCSuperIO.kext](https://github.com/acidanthera/VirtualSMC/releases) | VirtualSMC Plugin for Fan Speed Monitoring |
| [SMCBatteryManager.kext](https://github.com/acidanthera/VirtualSMC/releases) | VirtualSMC Plugin for Battery Monitoring |
| [HS80211Family.kext](https://www.insanelymac.com/forum/files/file/1008-io80211family-modif/?_fromLogin=1) | To Patch Qualcomm Atheros Wifi (For Activated [AirPortAtheros40.kext](https://www.insanelymac.com/forum/files/file/1008-io80211family-modif/?_fromLogin=1)) |
| [AirPortAtheros40.kext](https://www.insanelymac.com/forum/files/file/1008-io80211family-modif/?_fromLogin=1) | To Patch Qualcomm Atheros Wifi |
| [RealtekRTL8100.kext](https://www.insanelymac.com/forum/files/file/259-realtekrtl8100-binary/) | To Patch Realtek FE PCIe Family Ethernet |
| [VoodooI2C.kext](https://github.com/VoodooI2C/VoodooI2C/releases) | To Patch [VoodooI2CHID.kext](https://github.com/VoodooI2C/VoodooI2C/releases) I2C  Driver |
| [VoodooI2CHID.kext](https://github.com/VoodooI2C/VoodooI2C/releases) | To Patch Trackpad I2C Driver |
| [VoodooPS2Controller.kext](https://github.com/acidanthera/VoodooPS2/releases) | To Patch keyboard PS/2 Driver |


After you download it, copy and paste/replace all the kext to the EFI folder in EFI-> OC-> Kext)

### Used DSDT & SSDT : 

| DSDT / SSDT | Info | Guide |
| ----------- | ----------- | ----------- |
| [DSDT.aml](/EFI/OC/ACPI/DSDT.aml) | Differentiated System Description Table which contains the Differentiated Definition Block that supplies the implementation and configuration information about the base system | [Read](https://dortania.github.io/Getting-Started-With-ACPI/Manual/dump.html) |
| [SSDT-EC-USBX.aml](/EFI/OC/ACPI/SSDT-EC-USBX.aml) | Fix Embedded Controller for hotkeys and battery | [Read](https://dortania.github.io/Getting-Started-With-ACPI/Universal/ec-fix.html) |
| [SSDT-PLUG.aml](/EFI/OC/ACPI/SSDT-PLUG.aml) | Fix Intel Kabylake Processor Plugin Type | [Read](https://dortania.github.io/Getting-Started-With-ACPI/Universal/plug.html) |
| [SSDT-PNLF.aml](/EFI/OC/ACPI/SSDT-PNLF.aml)| Fix Backlight Slider | [Read](https://dortania.github.io/Getting-Started-With-ACPI/Laptops/backlight.html) |
| [SSDT-XOSI.aml](/EFI/OC/ACPI/SSDT-XOSI.aml)| Fix Trackpads | [Read](https://dortania.github.io/Getting-Started-With-ACPI/Laptops/trackpad.html) |

After you download it, copy and paste/replace all the DSDT/SSDT to the EFI folder in EFI-> OC-> ACPI)

### Installer MacOs, and Supporting App :

| Apps/Tools | Info | Link | Guide |
| ----------- | ----------- | ----------- | ----------- |
| gibMacOS | To get the installer | [Download](https://github.com/corpnewt/gibMacOS) | - |
| GenSMBIOS | To Generate a new Serial | [Download](https://github.com/corpnewt/gibMacOS) | [Read](https://dortania.github.io/OpenCore-Post-Install/universal/iservices.html#generate-a-new-serial) |
| ProperTree |  To configure OpenCore config.plist | [Download](https://github.com/corpnewt/ProperTree) | - |
| Clover Configurator | To configure Clover config.plist and Mount EFI Partition | [Download](https://mackie100projects.altervista.org/download-clover-configurator/) | - |
| SSDTTime | To get the DSDT and SSDT | [Download](https://github.com/corpnewt/SSDTTime) | [Read](https://dortania.github.io/Getting-Started-With-ACPI/ssdt-methods/ssdt-easy.html#running-ssdttime) |
| Hackintool | To see the device properties in macOS | [Download](https://github.com/headkaze/Hackintool/releases) | - |
| IntelPowerGadget | To see CPU Power Management and Performance test | [Download](https://software.intel.com/content/www/us/en/develop/articles/intel-power-gadget.html#attachment-heading) | - |