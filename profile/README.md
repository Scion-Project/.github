<p align="center"><img src="scion-logo.png" width="140" alt="Scion"></p>

<h1 align="center">Scion Project</h1>

<p align="center">Apple's open-source XNU kernel and iOS user space, grafted onto Android hardware.</p>

A *scion* is a cutting grafted onto another plant's rootstock. That is the idea here: the iPhone's software stack, running on phones it was never made for — with our own drivers underneath, and none of Apple's software in these repositories. Every image is built locally from your own IPSW.

### HakiOS — Exynos 9810 (Galaxy S9 / S9+ / Note9)

XNU booted straight on the hardware, with iOS 16.5 on top. On the Galaxy S9 today: all six usable cores with DVFS and thermal throttling, the AMOLED panel through the display controller's hardware scaler, touch, Mali-G72 GPU via Mesa Panfrost, native UFS storage with a persistent data volume, Wi-Fi joined from iOS Settings, the speakers, the front camera in the stock Camera app, the brightness slider, haptics, battery, and a USB log and console. Bluetooth, sensors, the microphone path, the modem and more are in progress.

| Repository | What it is |
|---|---|
| [hackios-xnu-kernel](https://github.com/Scion-Project/hackios-xnu-kernel) | The kernel, drivers, boot loader and tools (common to every device) |
| [hakios-starlte](https://github.com/Scion-Project/hakios-starlte) | Galaxy S9 device repository: configs, firmware facts, docs, porting record |
| [hakios-star2lte](https://github.com/Scion-Project/hakios-star2lte) · [hakios-crownlte](https://github.com/Scion-Project/hakios-crownlte) | Galaxy S9+ and Note9 (written, not yet run) |
| [scion-packaging](https://github.com/Scion-Project/scion-packaging) | Universal TWRP installer (tooling only) |
| [scion-recovery](https://github.com/Scion-Project/scion-recovery) | TWRP repurposed for HakiOS: APFS / HFS+ tools, log capture |

### Scion — Pixel 10

The same stack on the Google Pixel 10, emulated ([pyre](https://github.com/Scion-Project/pyre), a fast Apple-silicon emulator) or virtualised on the phone's own hypervisor ([scion-avf](https://github.com/Scion-Project/scion-avf)), from the [Scion](https://github.com/Scion-Project/scion) app.

---

Built on the work of the [HakiOS](https://github.com/oosexgang) and [ChefKiss](https://github.com/ChefKissInc) projects, Project Silicium, and the Exynos 9810 mainline community. Not affiliated with Apple, Samsung or Google.
