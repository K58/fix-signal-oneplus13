# fix-signal-oneplus13

Fix signal and bootloop for OnePlus 13 CN on OxygenOS 15 / 16.

[Download](https://github.com/K58/fix-signal-oneplus13/releases)

> [!WARNING]
> **PSA: Anti-Rollback Protection**
>
> OnePlus has implemented anti-rollback protection starting with firmware version **16.0.3.50x**.
>
> If you are on **16.0.3.50x or higher**, **DO NOT downgrade** to any earlier version (specifically the `xbl` bootloader partition):
> * This will cause a **HARD BRICK**.
> * **Leaked EDL tools will not work.** Anti-rollback is specifically designed to block them.
> * Only official/authorized EDL access can fix this state.
>
> Please be careful when flashing any ROMs.
>
> ~~Never Settle.~~ **Sometimes Settle.**

## Tutorial

### How to fix signal

Download and install this module in Magisk (or other root manager).

### How to fix bootloop

Make sure you have this module installed before OTA updates.

1. Finish an OTA system update, but DO NOT click Restart.

2. If you are updating to **OxygenOS 15**, press the "Action" button under the module name in Magisk (or other root manager), make sure the patch is successful.
    - Note: **OxygenOS 16** does not require bootloop fix. If you are updating to OxygenOS 16, you can skip this step and proceed to step 3.

3. You MUST also install Magisk (or other root manager) to inactive slot.
    - For Magisk: Magisk Manager -> Home -> Magisk (Install) -> Install to Inactive Slot (After OTA)

4. Press "Restart" in System Update

> [!WARNING]  
> **This module will modify `dtbo` partition to fix bootloop.** <br>
> Do NOT lock the bootloader with modified `dtbo` (or any other partition) in **any** slot.

### How to relock bootloader

**Please don't.**

Your device will **brick** if you relock the bootloader with any modifications to the system partition in **any** slot (e.g., root, dtbo, custom kernel, etc.).

> [!CAUTION]
> **This module is for rooted users. You **MUST** keep your bootloader unlocked. Do NOT lock the bootloader.** <br>
> 
> To relock the bootloader, you **MUST** remove root and restore the device to stock state.<br>
> **Relocking the bootloader is a dangerous operation.** Do not relock your bootloader unless you fully understand what you are doing.<br>
> On OnePlus 13, you cannot access fastboot again via key combination if the bootloader is locked.<br>
> If you lock your bootloader while rooted or modified, your phone will hard brick and cannot be recovered by yourself.
>
> If **any** of the following are not met, relocking the bootloader **will brick your device**:
>
> * **Do not trigger anti-rollback protection. Please read [the warning](https://github.com/K58/fix-signal-oneplus13#:~:text=PSA%3A-,Anti%2DRollback%20Protection,-OnePlus%20has%20implemented) above.**
> * **Every system partition in BOTH slots must be 100% stock and unmodified.**
>   * To ensure this, after restoring the latest version of stock OS on your device, download the full OTA ROM (.zip) for that OS version and local install it TWICE: local install, then reboot, then local install it AGAIN.
>   * Be very careful when rolling back to an older OS version. If your device has upgraded to an OS version with anti-rollback, downgrading to any earlier version will brick it.
> * **Google account must be removed.**
>   * On older ColorOS / OxygenOS versions, due to a critical bug, FRP (Factory Reset Protection, a.k.a. activation lock) prevents completing the initial setup, effectively bricking it.

----

## Thanks to

- [@koaaN](https://xdaforums.com/m/koaan.3433581/)

- [@docnok63](https://xdaforums.com/m/docnok63.4967345/)

- [rapperskull](https://github.com/rapperskull)

