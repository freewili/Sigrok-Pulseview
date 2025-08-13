# Installation

1. Execute the appropriate installer for your system. pulseview-installer-32.exe for 32-bit windows, pulseview-installer-64.exe for 64-bit windows.

2. Follow the on-screen prompts to complete the installation.

3. Once installed, you can launch PulseView by searching for **PulseView** in the Windows Start menu or search bar.

---

# Detecting the FREE-WILi Logic Analyzer

To ensure PulseView detects the FREE-WILi device correctly, you may need to update the device drivers using **Zadig**.

### What is Zadig?

Zadig is a utility for installing generic USB drivers such as WinUSB, libusb-win32, or libusbK, which are required for PulseView to communicate with many USB logic analyzers.

**Be very careful at this step.** Incorrectly modifying the driver for other devices connected to your computer can cause them to stop working.

---

### Steps to update the FREE-WILi driver using Zadig:

1. Launch Zadig. It was installed along with Pulseview.

2. From the **Options** menu, enable **List All Devices**.

3. In the device dropdown list, locate the device named **FreeWili**.
> If it is not in the list, ensure your FREE-WILi is connected to the computer.

4. Select **WinUSB** as the target driver.

5. Click **Replace Driver** (or **Install Driver** if no driver is currently installed).

6. Once the driver installation completes, close Zadig.

---

### Using FREE-WILi with PulseView

- Open PulseView.

- In the device selection menu, choose the **FREE-WILi (fwili)** driver.

- If your FREE-WILi device is connected, PulseView should now detect it.

>**NOTE:** The FREE-WILi will be detected by two sigrok drivers - FTDI LA and FREE WILi.
> Ensure the logic analyzer view only has four channels to confirm you are using the correct driver.
---

### FPGA Configuration Notes

- The FREE-WILi’s FPGA configuration determines which pins and protocols are monitored by default.

- The default monitoring mode is **SPI**.

- You can reconfigure the FPGA to monitor other protocols such as **UART** or **I2C** with GPIO pins 26 and 27 on the main processor.

---

If you encounter any issues with detection or driver installation, please consult the PulseView documentation or reach out for support.
