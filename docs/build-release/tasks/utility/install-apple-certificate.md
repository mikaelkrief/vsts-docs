---
title: Install Apple Certificate
description: Install an Apple certificate required to build on a macOS agent on VSTS and Team Foundation Server TFS
ms.prod: vs-devops-alm
ms.technology: vs-devops-build
ms.assetid: d2eff759-736d-4b7b-8554-7ba0960d49d6
ms.manager: dastahel
ms.author: madhurig
ms.date: 05/22/2017
---

# Utility: Install Apple Certificate

**VSTS**

![](../build/_img/xcode-build.png) Install an Apple certificate required to build on a macOS agent

This task allows installing an Apple certificate that is stored as a [secure file](../../concepts/library/secure-files.md) on the server. 

## Demands

xcode

## Agent version

2.116.0 or higher is required

## Arguments

| Argument | Description |
| -------- | ----------- |
| Certificate (P12) | Select the certificate (.p12) that was uploaded to **Secure Files** to install on the macOS agent. |
| Certificate (P12) Password | Password to the Apple certificate (.p12). Use a new build variable with its lock enabled on the **Variables** tab to encrypt this value. |
| Advanced - Keychain | Select the keychain in which to install the Apple certificate. You can choose to install the certificate in a temporary keychain (default), the default keychain or a custom keychain. A temporary keychain will always be deleted after the build or release is complete. |
| Advanced - Keychain Password | Password to unlock the keychain. Use a new build variable with its lock enabled on the **Variables** tab to encrypt this value. A password is generated for the temporary keychain if not specified. |
| Advanced - Delete Certificate from Keychain | Select to delete the certificate from the keychain after the build or release is complete. This option is visible when custom keychain or default keychain are selected. |
| Advanced - Custom Keychain Path | Full path to a custom keychain file. The keychain will be created if it does not exist. This option is visible when a custom keychain is selected. |
| Advanced - Delete Custom Keychain | Select to delete the custom keychain from the agent after the build or release is complete. This option is visible when a custom keychain is selected. |
