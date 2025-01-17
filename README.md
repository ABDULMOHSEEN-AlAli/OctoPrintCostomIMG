# OctoPrintCustomIMG

## Introduction

This repository contains a modified version of the OctoPrint-Cam IMG which is available in the Raspberry Pi Imager. The custom IMG includes several enhancements aimed at improving functionality and compatibility.

### Enhancements:
- **Updated "apt" version**: The package manager has been updated to ensure better compatibility and smoother operations.
- **Enabled Legacy Camera Support**: Adjustments to the `raspi-config` file to allow the use of legacy camera modules.
- **Camera Configuration**: Modifications made to the `/boot/config.txt` file to configure the camera settings:
    ```bash
    camera_auto_detect=0
    dtoverlay=imx219
    ```
- **Network Configuration**: Updates to the `octopi-wpa-supplicant.txt` file to configure network access to your local network. *(Note: You need to change the network information to match your local network setup.)*

## Instructions

### 1. **Install the IMG file**:
   - You can do this by running `git clone https://github.com/ABDULMOHSEEN-AlAli/OctoPrintCostomIMG.git`

### 2. **Edit the Network Access Configuration**:
   - The `octopi-wpa-supplicant.txt` file should be updated for network access. Make sure to replace the placeholder values with your network details:
     - SSID: Your network's name
     - Password: Your network's password

   Example:
   `bash
   network={
       ssid="YourNetworkSSID"
       psk="YourNetworkPassword"
   }`

### 3. **Copy the IMG**:
  - Use Raspberry Pi Imager app to write the IMG to your SD card then you will be done.

*Note: This IMAGE is dedicated for Raspberry Pi 4B and it may not work properly on different versions*
