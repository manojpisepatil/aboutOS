
# Flashing TWRP and Disabling Encryption on Xiaomi Mi A2

This repository provides a step-by-step guide for flashing the TWRP custom recovery and disabling encryption on the Xiaomi Mi A2. Follow these instructions carefully to unlock your device's bootloader, flash TWRP, and manage encryption.

## Prerequisites
Before you begin, ensure the following files are copied to your C: drive:
- **Platform Tools**: The zipped and extracted files.
- **TWRP Image**: The TWRP image file.
- **Disable Encryption File**: The Disable Dm-Verify ForceEncrypt file.
- **ADB Setup**: Installed ADB and fastboot tools.

## Step 1: Unlock the Bootloader
1. Open Command Prompt (cmd) through platform tools folder.
2. Verify your device is recognized with:
   ```
   fastboot devices
   ```
3. Check if the bootloader is locked:
   ```
   fastboot oem device-info
   ```
   (should return `false` if locked)
4. Unlock the bootloader:
   ```
   fastboot oem unlock
   ```
   or
   ```
   fastboot flashing unlock
   ```
5. Confirm the bootloader is unlocked:
   ```
   fastboot oem device-info
   ```
   (should return `true`)

## Step 2: Alternate Method if Step 1 Fails
1. Open Command Prompt (cmd).
2. Verify your device is recognized with:
   ```
   fastboot devices
   ```
3. Check the bootloader status:
   ```
   fastboot oem device-info
   ```
   (should return `false` if locked)
4. Unlock critical partitions:
   ```
   fastboot flashing unlock
   fastboot flashing unlock_critical
   ```
5. Confirm the bootloader is unlocked:
   ```
   fastboot oem device-info
   ```
   (should return `true`)

## Additional Steps to Prevent TWRP Boot Issues
1. Format userdata:
   ```
   fastboot format userdata
   ```
2. Format cache:
   ```
   fastboot format cache
   ```
3. Boot into TWRP:
   ```
   fastboot boot "path to TWRP file"
   ```

## Flashing TWRP and Disabling Encryption
1. Once in TWRP, copy the TWRP image and Disable Dm-Verify ForceEncrypt zip file to your device.
2. Flash the TWRP image to the recovery partition.
3. Flash the Disable Dm-Verify ForceEncrypt zip file.
4. Reboot into the system from the TWRP home menu.

## Completion
Your Xiaomi Mi A2 should now have TWRP installed and encryption disabled, ready for further customization.
