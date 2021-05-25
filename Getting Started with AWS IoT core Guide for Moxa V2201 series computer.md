# Getting Started with AWS IoT core Guide for Moxa V2201 series computer

# Document Information

## Revision History (Version, Date, Description of change)

| Version | Date        | Description of change |
| ------- | ----------- | --------------------- |
| 1       | 2021/04/19 | First release         |
|         |             |                       |

# Overview

The Moxa V2201 Series ultra-compact x86 embedded computer is based on the Intel® Atom™ E3800 Series processor, features the most reliable I/O design to maximize connectivity, and supports dual wireless modules, making it suitable for a diverse range of communication applications. The computer’s thermal design ensures reliable system operation in temperatures ranging from -40 to 85°C, and wireless operation in temperatures ranging from -40 to 70°C with a special purpose Moxa wireless module installed. The V2201 Series supports “Moxa Proactive Monitoring” for device I/O status monitoring and alerts, system temperature monitoring and alerts, and system power management. Closely monitoring the system status makes it easier to recover from

# Hardware Description

## DataSheet

[V2201 series](https://www.moxa.com/getmedia/7e1bd1db-3ee2-4bd9-9494-7fa61ced8d4c/moxa-v2201-series-datasheet-v2.5.pdf)

## Standard Kit Contents

The standard shipping Moxa V2201 series computer package contains the following items:

- 1 x V2201 embedded computer
- 1 x Terminal block to power jack converter
- 1 x Wall mounting kit
- 1 x Quick installation guide (printed)
- 1 x Warranty card

## User Provided items

To setup and operate Moxa V2201 series computer, users have to prepare the following items by themselves.

- 10/100/1000M Ethernet cables
- Power adapter: input voltage 90 to 264 VAC, output voltage 24 V with 2.5 A DC load (can be purchased separately from Moxa)
- Power Cord: Power cord with AU/CN/EU/UK/US plug, 2.5A/250V, 1.83 m (can be purchased separately from Moxa)

Based on user’s application requirement, the following items are optional

- WiFi or Cellular module (can be purchased separately from Moxa)
- Antennas (can be purchased separately from Moxa)

## 3rd Party purchasable items
N/A

# Set up your Hardware Environment
- **Connecting a Display**

    Moxa V2201 series computer comes with HDMI interfaces on the rear panel. Connect a display monitor to the HDMI interfaces.

- **Connecting a Keyboard and Mouse**

    Connectors for a keyboard and mouse are located on the rear panel of the computer. Both connectors are USB interfaces; you can directly connect a keyboard and a mouse using these connectors.

- **Powering on Moxa V2201 series computer :**

    To power on the V2201, connect the “terminal block to power jack converter” to the V2201’s DC terminal block (located on the side panel),and then connect the 9 to 36 VDC power adapter. The computer will be automatically turned on once the power adapter is plugged in. If it does not, press the Power Button to turn on the computer. Note that the Shielded Ground wire should be connected to the top pin of the terminal block. It takes about 30 seconds for the system to boot up. Once the system is ready, the Power LED will light up.
- **Accessing Moxa V2201 series computer Using a Linux/Windows PC or Mac**

    You can use a PC to access Moxa V2201 series ****computer by using SSH over the network. Refer to the following IP addresses and login information:

    ![images/image2.png](images/image2.png)

Login: moxa

Password: moxa

Root account login is disabled until you manually create a password for the account. The user moxa is in the sudo group so you can operate system level commands with this user using the sudo command.

**ATTENTION: For security reasons, we recommend that you disable the default user account and create your own user accounts or** 

**Refer to Account Management of [Moxa V2201 series computer-linux-user-manual](https://www.moxa.com/getmedia/9ba97e7e-9c71-40d0-8c07-c6865ce24e97/moxa-v2201-series-linux-manual-v2.0.pdf) for the detail steps.**

- **Change the network settings of Moxa V2201 series computer based on your network environment**

    Refer to the Changing the interfaces Configuration File of [Moxa V2201 series computer-linux-user-manual](https://www.moxa.com/getmedia/9ba97e7e-9c71-40d0-8c07-c6865ce24e97/moxa-v2201-series-linux-manual-v2.0.pdf) for the detail steps.

# Set up your Development Environment

## Tools Installation (IDEs, Toolchains, SDKs)

The operation system of Moxa V2201 series is a native 64-bits X86 Linux operating system. There is no need to install toolchains. You can install development tools in Moxa V2201 series computer directly.

Follow these steps to update the package menu:

1. Make sure a network connection is available.

2. Use apt-get update to update the Debian package list.

```bash
moxa@Moxa:~$ sudo apt-get update
```

3. Install the native compiler and necessary packages.

```bash
moxa@Moxa:~$ sudo apt-get install gcc build-essential flex bison automake
```

# Setup your AWS account and Permissions

Refer to the instructions at [Set up your AWS Account](https://docs.aws.amazon.com/iot/latest/developerguide/setting-up.html). Follow the steps outlined in these sections to create your account and a user and get started:

- Sign up for an AWS account and
- Create a user and grant permissions.
- Open the AWS IoT console

Pay special attention to the Notes.

# Create Resources in AWS IoT

Refer to the instructions at [Create AWS IoT Resources](https://docs.aws.amazon.com/iot/latest/developerguide/create-iot-resources.html). Follow the steps outlined in these sections to provision resources for your Moxa V2201 series computer:

- Create an AWS IoT Policy
- Create a thing object

Pay special attention to the Notes.

> **Important**
Before you continue to the next step, your Moxa computer must be configured, and running. The Moxa computer must be connected to the Internet and you will need to be able to access the computer by using its command line interface. Command line access can be through SSH terminal remote interface.

# Build the demo

Follow above section, **Accessing Moxa V2201 series** **computer Using a Linux/Windows PC or Mac,** using PuTTY to open a remote terminal to Moxa computer on **Linux/Windows PC or Mac** and perform the following instructions in that window. 

Refer to the instruction at [Install the required tools and libraries for the AWS IoT Device SDK](https://docs.aws.amazon.com/iot/latest/developerguide/connecting-to-existing-device.html#gs-device-sdk-tools) and [Install AWS IoT Device SDK](https://docs.aws.amazon.com/iot/latest/developerguide/connecting-to-existing-device.html#gs-device-install-sdk) for Python on Moxa V2201 series computer directly. Follow the steps outlined in these sections to install AWS IoT Device SDK for your Moxa computer:

- Update the operating system and install required libraries
- Install git
- Install the AWS IoT Device SDK for Python.

Note: Due to using Python, there is no need to compile/build any programs. And we perform all steps in Moxa computer, there is no need to load/upload any programs to it.

# Run the demo

Continue previous section, perform the instructions, [Install and run the sample app](https://docs.aws.amazon.com/iot/latest/developerguide/connecting-to-existing-device.html#gs-device-node-app-run), in that terminal window. 

To view the MQTT messages published by the sample app in the AWS IoT console, perform the instructions,[View messages from the sample app in the AWS IoT console](https://docs.aws.amazon.com/iot/latest/developerguide/connecting-to-existing-device.html#gs-device-view-msg).

# Debugging

1. Not able to login Moxa V2201 series computer's through SSH terminal.

    Connect a display monitor to the Moxa V2201 series computer, and then power it up. Once the system is ready, a login screen will appear on your monitor. Refer to Starting from a VGA Console of [**Moxa V2201 series computer-linux-user-manual](https://www.moxa.com/getmedia/9ba97e7e-9c71-40d0-8c07-c6865ce24e97/moxa-v2201-series-linux-manual-v2.0.pdf)** for the detail steps. After login Moxa computer check following items:

    a. Check if IP address of LAN1/LAN2 is in the same subnet of your PC.

    b. Check if you are able to operate OS normally. If not, gather all error message when you operate OS and then [CONTACT US](https://www.moxa.com/en/support/technical-support)

2. Moxa computer is not able to access internet.

    a. Check if IP address, mask and gateway of LAN1/LAN2 are configured in /etc/network/interfaces properly.

    b. Check if routing is correct.

    c. Check if nameserver is configured in /etc/resolv.conf

# Troubleshooting

Still need assistance with your Moxa product? [CONTACT US](https://www.moxa.com/en/support/technical-support)
