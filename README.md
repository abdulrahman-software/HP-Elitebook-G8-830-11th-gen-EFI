# HP EliteBook 830 G8 Hackintosh EFI

OpenCore EFI for the HP EliteBook 830 G8 (Intel).

## Tested and working

On macOS Big Sur, the author reports that these work:

- Intel graphics hardware acceleration
- Internal keyboard
- Trackpad
- Audio
- Wi-Fi through AirportItlwm

Big Sur is the only macOS version reported as fully working with this EFI.

## Other macOS versions tried

macOS Sequoia and macOS Tahoe were also tried, but Intel graphics hardware acceleration did not work. They are not supported by this EFI.

## Graphics project credit

Graphics support uses [WhateverXe](https://github.com/b00t0x/WhateverXe), a Lilu plugin adapting Apple's graphics drivers for supported Intel Xe-LP integrated GPUs. Many thanks to the WhateverXe contributors for their work.

## Wi-Fi

This EFI uses AirportItlwm. The separate `itlwm.kext` has been removed. Saved Wi-Fi network names and passwords have also been removed from the public EFI.

## Before use

This public copy has sanitized SMBIOS placeholders. Generate your own SMBIOS values and set `PlatformInfo -> Generic -> MLB`, `ROM`, `SystemSerialNumber`, and `SystemUUID` in `OC/config.plist` before booting. Never publish or reuse another person's SMBIOS values.

This EFI is hardware-specific. Review the configuration and replace the SMBIOS placeholders for your own machine before using it.
