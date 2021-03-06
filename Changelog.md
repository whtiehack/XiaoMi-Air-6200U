# Xiaomi Mi Air 13.3 Skylake-U 2016

- 06-01-2019

    - Initial Release

- 20-01-2019

    - Added Benchmarks @ README.md
    - Removed SSDT-PNP0C14.aml (not sure why I should use it)
    - change EC0 to EC config.plist patch (SSDT-USBX.dsl) and removed SSDT-EC.dsl (check [article](https://www.tonymacx86.com/threads/guide-usb-power-property-injection-for-sierra-and-later.222266/) )
    - removed SSDT-BKEY.dsl (from JahStories) and use SSDT-BCKS.dsl based on [this](https://www.tonymacx86.com/threads/guide-patching-dsdt-ssdt-for-laptop-backlight-control.152659/)
    - Tested HDMI
    - Played with HiDPI and decided not to use it since it does not make sense

- 02-02-2019

    - HackingTool used `/CLOVER/kexts/Other/USBPorts.kext`. This patch includes power injection as well (remove `SSDT-USBX.aml`)

- 01-08-2019

    - updated for `10.14.6`
    - upgrade clover to `Clover_v2.5k_r5033`
    - `AptioInputFix.efi` from acidanthera/AptioFixPkg AptioFix-R27-RELEASE.zip
    - `AptioMemoryFix.efi` from acidanthera/AptioFixPkg AptioFix-R27-RELEASE.zip
    - `ApfsDriverLoader.efi` from acidanthera/AppleSupportPkg AppleSupport-v2.0.8-RELEASE.zip
    - `AppleUiSupport.efi` from acidanthera/AppleSupportPkg AppleSupport-v2.0.8-RELEASE.zip
    - upgrade to `Lilu.1.3.7.RELEASE.zip`
    - upgrade to `AppleALC.1.3.9.RELEASE.zip`
    - upgrade to `CPUFriend.1.1.8.RELEASE.zip`
    - upgrade to `HibernationFixup.1.2.6.RELEASE.zip`
    - upgrade to `VirtualSMC.1.0.6.RELEASE.zip`
    - upgrade to `WhateverGreen.1.3.0.RELEASE.zip`
    - upgrade to `acidanthera/VoodooPS2 (2.0.1.1)` from RehabMan-Voodoo-2018-1008.zip
    - Remove `SSDT-PNLF.dsl` and replace with `AddPNLF` argument and `SetIntelBacklight` and `SetIntelMaxBacklight` as suggested in [WhateverGreen FAQ](https://github.com/acidanthera/WhateverGreen/blob/master/Manual/FAQ.IntelHD.en.md#adjusting-the-brightness-on-a-laptop)
    - Remove `ACPIBatteryManager.kext` and used `SMCBatteryManager.kext` as noted [here](https://github.com/daliansky/XiaoMi-Pro-Hackintosh/pull/204)
    - Remove `SSDT-DDGPU` because disable-external-gpu does the same thing
    - Change igfxrst=1 to gfxrst=1 according to [WhateverGreen README](https://github.com/acidanthera/WhateverGreen/blob/master/README.md)
    - Added `darkwake=0` based on [daliansky/XiaoMi-Pro-Hackintosh](https://github.com/daliansky/XiaoMi-Pro-Hackintosh)
    - Remove `-cdfon` based on [daliansky/XiaoMi-Pro-Hackintosh](https://github.com/daliansky/XiaoMi-Pro-Hackintosh)
    - Remove `GFX0 -> IGPU`, `HECI -> IMEI`, and `HDAS -> HDEF` according to [WhateverGreen FAQ.IntelHD](https://github.com/acidanthera/WhateverGreen/blob/master/Manual/FAQ.IntelHD.en.md#adjusting-the-brightness-on-a-laptop)
    - devices have been added in config.plist from the Hackingtool/PCItab and exported
    - Remove SSDT-PXSX and move device properties to config.plist
    - update `SSDT-HPET.dsl` based on [daliansky/XiaoMi-Pro-Hackintosh](https://github.com/daliansky/XiaoMi-Pro-Hackintosh)
    - update `SSDT-MEM2.dsl` based on [daliansky/XiaoMi-Pro-Hackintosh](https://github.com/daliansky/XiaoMi-Pro-Hackintosh)
    - update `SSDT-PMCR.dsl` based on [daliansky/XiaoMi-Pro-Hackintosh](https://github.com/daliansky/XiaoMi-Pro-Hackintosh)

- 26-02-2020

    - updated for `10.15.3`
    - upgrade clover to `Clover_v2.5k_r5099`
    - `EFI/CLOVER/drivers/UEFI/ApfsDriverLoader.efi` from [z390 guide](https://www.tonymacx86.com/threads/success-gigabyte-designare-z390-thunderbolt-3-i7-9700k-amd-rx-580.267551/page-1131#post-2046300)
    - `EFI/CLOVER/drivers/UEFI/AudioDxe.efi` from [z390 guide](https://www.tonymacx86.com/threads/success-gigabyte-designare-z390-thunderbolt-3-i7-9700k-amd-rx-580.267551/page-1131#post-2046300)
    - `EFI/CLOVER/drivers/UEFI/EmuVariableUefi.efi` from [z390 guide](https://www.tonymacx86.com/threads/success-gigabyte-designare-z390-thunderbolt-3-i7-9700k-amd-rx-580.267551/page-1131#post-2046300)
    - `EFI/CLOVER/drivers/UEFI/FwRuntimeServices.efi` from [z390 guide](https://www.tonymacx86.com/threads/success-gigabyte-designare-z390-thunderbolt-3-i7-9700k-amd-rx-580.267551/page-1131#post-2046300)
    - `EFI/CLOVER/drivers/UEFI/HFSPlus.efi` from [z390 guide](https://www.tonymacx86.com/threads/success-gigabyte-designare-z390-thunderbolt-3-i7-9700k-amd-rx-580.267551/page-1131#post-2046300)
    - `EFI/CLOVER/drivers/UEFI/OcQuirks.efi` from [z390 guide](https://www.tonymacx86.com/threads/success-gigabyte-designare-z390-thunderbolt-3-i7-9700k-amd-rx-580.267551/page-1131#post-2046300)
    - `EFI/CLOVER/drivers/UEFI/OcQuirks.plist` from [z390 guide](https://www.tonymacx86.com/threads/success-gigabyte-designare-z390-thunderbolt-3-i7-9700k-amd-rx-580.267551/page-1131#post-2046300)
    - `EFI/CLOVER/drivers/UEFI/UsbKbDxe.efi` from [z390 guide](https://www.tonymacx86.com/threads/success-gigabyte-designare-z390-thunderbolt-3-i7-9700k-amd-rx-580.267551/page-1131#post-2046300)
    - `EFI/CLOVER/drivers/UEFI/UsbMouseDxe.efi` from [z390 guide](https://www.tonymacx86.com/threads/success-gigabyte-designare-z390-thunderbolt-3-i7-9700k-amd-rx-580.267551/page-1131#post-2046300)
    - `EFI/CLOVER/drivers/UEFI/VirtualSmc.efi` from [z390 guide](https://www.tonymacx86.com/threads/success-gigabyte-designare-z390-thunderbolt-3-i7-9700k-amd-rx-580.267551/page-1131#post-2046300)
    - `EFI/CLOVER/drivers/UEFI/AppleGenericInput.efi` FileVault support from [The Vanilla Laptop Guide](https://fewtarius.gitbook.io/laptopguide/extras/enabling-filevault) from acidanthera/AppleSupportPkg AppleSupport-v2.0.9-RELEASE.zip
    - `EFI/CLOVER/drivers/UEFI/AppleUiSupport.efi` FileVault support from [The Vanilla Laptop Guide](https://fewtarius.gitbook.io/laptopguide/extras/enabling-filevault) from acidanthera/AppleSupportPkg AppleSupport-v2.0.8-RELEASE.zip
    - upgrade to `Lilu.1.4.1.RELEASE.zip`
    - upgrade to `AppleALC.1.4.6.RELEASE.zip`
    - upgrade to `CPUFriend.1.2.1.RELEASE.zip`
    - upgrade to `HibernationFixup.1.3.2.RELEASE.zip`
    - upgrade to `VirtualSMC.1.0.9.RELEASE.zip`
    - upgrade to `WhateverGreen.1.3.6.RELEASE.zip`
    - upgrade to `acidanthera/VoodooPS2 (VoodooPS2Controller-2.1.1)`
    - upgrade to `acidanthera/VoodooPS2 (VoodooInput-1.0.2)`
    - bluetooth injection `IntelBluetooth.1.0.2.zip`
    - added small guide on readme for upgrading from `10.14.6` to `10.15.3`

- 28-02-2020

    - new `CPUFriendDataProvider.kext` based on [corpnewt/CPUFriendFriend](https://github.com/corpnewt/CPUFriendFriend) with min hex freq 800Mhz=08 and EPP Range: (0x80-0xBF:Balance power) = 80
    - updated Benchmarks for `10.15.3`
    - added `TP-Link_Installer_Mac 10.15_Beta.zip Published Date: 2019-11-22` from [tplink](https://www.tp-link.com/us/support/download/archer-t3u/#Driver)

- 06-11-2020

    - migrated from `Clover` to `OpenCore 0.6.2`
    - tested for `10.15.3`
    - upgraded and tested for `10.15.7`
    - updated guide
    - upgrade to `VirtualSMC-1.1.7`
    - upgrade to `Lilu-1.4.8`
    - upgrade to `AppleALC-1.5.3`
    - upgrade to `WhateverGreen-1.4.3`
    - upgrade to `NVMeFix-1.0.4`
    - upgrade to `CPUFriend-1.2.2`
    - upgrade to `VoodooPS2Controller-2.1.8`
    - usage of `corpnewt/CPUFriendFriend`
    - usage to `RehabMan/OS-X-Null-Ethernet`
    - fix headphone port with `hackintosh-stuff/ComboJack`
    - updated Benchmarks
    - population DeviceProperties @ config.plist
    - clean up repository

- 15-11-2020

    - migrated from `OpenCore 0.6.2` to `OpenCore 0.6.3`
    - tested for `Catalina 10.15.7`
    - upgraded and tested for `Big Sur 11.0.1`
    - remove `RehabMan/OS-X-Null-Ethernet` and use `OpenIntelWireless` for native wifi support
    - upgrade to `VirtualSMC-1.1.8`
    - upgrade to `Lilu-1.4.9`
    - upgrade to `AppleALC-1.5.4`
    - upgrade to `WhateverGreen-1.4.4`
    - usage of `itlwm_v1.1.0_Stable`
    - updated Benchmarks for 11.0.1

- 16-12-2020

    - migrated from `OpenCore 0.6.3` to `OpenCore 0.6.4`
    - upgraded from `Big Sur 11.0.1` to `Big Sur 11.1`
    - upgrade to `Lilu-1.5.0`
    - upgrade to `AppleALC-1.5.5`
    - upgrade to `WhateverGreen-1.4.5`
    - upgrade to `VirtualSMC-1.1.9`
    - upgrade to `VoodooPS2Controller-2.1.9`
    - added `SSDT-Swap-LeftControlCapsLock.dsl` but did not used it
