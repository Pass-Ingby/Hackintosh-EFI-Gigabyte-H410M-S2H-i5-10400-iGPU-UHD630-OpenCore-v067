I am not a specialist and I spend a lot of time to make my system work.

In my opinion, I assume that it is a very common low budget combination.

So, I am placing here my files to save you some time.

You have to import your custom System Serial, UUID, and MLB numbers.

Working everything except sleep/wake (you have to unplug and plug the display cable).

Easy fix = Disable your display turn off in power settings.

Of course, if anyone find an 100% solution, I will be gratefully to hear about it.

There are two versions:

Final = For exactly same system with theme, modded USB3 and LAN kexts
(The OpenShell and Clear NVRAM tools are hidden under spacebar)

Debug = For experiments on similar systems with detailed debug info and original clear kexts
(You will probably need to generate your own ACPI SSDTs)


=============================== SYSTEM SPECIFICATIONS  ===============================

Motherboard: Gigabyte H410M-S2H

CPU: Intel i5-10400

GPU: Intel UHD630 (internal)

RAM: HyperX 16GB (2666MHz)

M2: ADATA NVMe 256GB


=============================== ESSENTIAL BIOS SETTING ===============================

0. Load Optimized Defaults (Save & Exit)
1. Favorites -> Extreme Memory Profile (XMP) = Enabled or Profile1 (if RAM is above 2400MHz)
2. Favorites -> CSM Support = Disabled
3. Favorites -> Secure Boot Mode = Disabled or Custom
4. Favorites -> SATA Controllers = Enabled
5. Settings -> IO Ports -> Initial Display Output = IGFX
6. Settings -> IO Ports -> Internal Graphics = Enabled
7. Settings -> IO Ports -> DVMT Pre-Allocated = 64M - 128M
8. Settings -> IO Ports -> DVMT Total Gfx Mem = Up to 1024M
9. Settings -> IO Ports -> Super IO Configuration -> Serial Port = Disabled
10. Settings -> IO Ports -> USB Configuration -> All 3 settings = Enabled
11. Settings -> IO Ports -> Network Stack = Disabled
12. Settings -> IO Ports -> SATA Configuration -> SATA mode = AHCI
13. Boot -> CFG Lock = Disabled
14. Boot -> Security Option = System
15. Boot -> Fast Boot = Disabled link
16. Boot -> Windows 10 Features = Other OS

* There is no need to disable VT-d
 
* You can enable Above 4G Decoding if you want


=============================== EXTRA DETAILS ===============================

1. Due to security reasons Apple does not allow non certificated extensions to get installed.
   So, I have put NVRAM/Add/7C436110-AB2A-4BBB-A880-FE41995C9F82/csr-active-config = 03000000.
   You can change it to 00000000 if you facing updating problems.

2. If you experience boot loop after partition scheme modification consider of changing the SecureBoot flags (not tested).
