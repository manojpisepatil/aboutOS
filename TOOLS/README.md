# TOOLS Directory

Welcome to the `TOOLS` directory of the `aboutOS` project! This directory contains essential utilities for managing and configuring the aboutOS operating system. Below are the details and usage instructions for each file available in this directory.

## Files Overview

### 1. **UniversalAdbDriverSetup.msi**

**Purpose:**  
`UniversalAdbDriverSetup.msi` is a Windows installer package for installing universal ADB (Android Debug Bridge) drivers. This driver is crucial for establishing a connection between your Android device and your computer, enabling debugging and file transfers.

**How to Install:**
- Double-click the `UniversalAdbDriverSetup.msi` file to begin the installation.
- Follow the on-screen instructions to complete the setup.
- Once installed, your Android device should be recognized when connected via USB.

### 2. **adb-setup-1.3.exe**

**Purpose:**  
`adb-setup-1.3.exe` is a one-click installer for ADB, Fastboot, and the required drivers. It simplifies the process of setting up ADB and Fastboot on your Windows machine.

**How to Install:**
- Double-click the `adb-setup-1.3.exe` file to launch the installer.
- When prompted, press 'Y' to install ADB and Fastboot.
- Follow the prompts to install the necessary drivers.
- After installation, you can use ADB and Fastboot from any command prompt.

**Example Commands:**
- To check if your device is connected:
    ```bash
    adb devices
    ```
- To reboot your device into bootloader mode:
    ```bash
    adb reboot bootloader
    ```

## Contributing

We welcome contributions to this directory! If you have utilities that can enhance the functionality of aboutOS, feel free to submit a pull request. Please ensure that your contributions are documented and maintain consistency with the existing tools.
