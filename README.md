# Unity DirectInput Force Feedback

[![Made with Unity](https://img.shields.io/badge/Made%20with-Unity-57b9d3.svg?style=for-the-badge&logo=unity)](https://unity3d.com)
![GitHub issues open](https://img.shields.io/github/issues/MrTimcakes/Unity-DirectInput?style=for-the-badge)
![GitHub issues close](https://img.shields.io/github/issues-closed/MrTimcakes/Unity-DirectInput?style=for-the-badge)
![GitHub package.json version](https://img.shields.io/github/package-json/v/MrTimcakes/Unity-DirectInput?style=for-the-badge)
![GitHub](https://img.shields.io/github/license/MrTimcakes/Unity-DirectInput?style=for-the-badge)

![Unity-DirectInput Banner](https://github.com/MrTimcakes/Unity-DirectInput/blob/assets/UnityDirectInputBanner.png )

This package allows you to easily integrate both the input and ForceFeedback features of DirectX DirectInput from within Unity. This allows you to interface with HID peripherals with ForceFeedback capabilities. This can be used to build vivid simulated experiences.

The package will create a virtual device inside Unity's Input System. This device can then be used like any other device inside the Input System, allowing for easy rebinding. ForceFeedback capabilites can be accessed via the DIManager class. The [DirectInputExplorer](../../tree/main/DirectInputExplorer~) is a windows forms application built in parallel with the C++ library to enable quick development by avoiding the need to reload Unity after every change. It also functions as an easy way to examine DirectInput devices.

# Quick Start

### Installation

This package requires use of Unity's new Input System, ensure [com.unity.inputsystem](https://docs.unity3d.com/Packages/com.unity.inputsystem@1.0/manual/QuickStartGuide.html) is installed in the project. Install it via the package manager via: 

`Window -> Package Manager => Input System`

Next, install this package:

`Package Manager => + => "Add package from git URL..." => ` `https://github.com/MrTimcakes/Unity-DirectInput.git` 


## Supported ForceFeedback Effects

| Effect        | Supported |
|---------------|-----------|
| ConstantForce | ✅ |
| CustomForce   | 🔲 |
| Damper        | ✅ |
| Friction      | ✅ |
| Inertia       | ✅ |
| RampForce     | 🔲 |
| SawtoothDown  | 🔲 |
| SawtoothUp    | 🔲 |
| Sine          | 🔲 |
| Spring        | ✅ |
| Square        | 🔲 |
| Triangle      | 🔲 |

[comment]: <> (✅ 🔲)

## Compatible Devices

| Peripheral                         | Test Status    |
|------------------------------------|----------------|
| [Fanatec CSL Elite](https://fanatec.com/eu-en/racing-wheels-wheel-bases/wheel-bases/csl-elite-wheel-base-officially-licensed-for-playstation) | ✅ Verified    |
| [Fanatec CSW V2.0](https://fanatec.com/eu-en/racing-wheels-wheel-bases/wheel-bases/clubsport-wheel-base-v2-servo) | ✅ Verified    |
| [Fanatec WRC Wheel Rim](https://fanatec.com/eu-en/steering-wheels/csl-elite-steering-wheel-wrc) | ✅ Verified    |
| [Fanatec Formula V2 Wheel Rim](https://fanatec.com/eu-en/steering-wheels/clubsport-steering-wheel-formula-v2) & [APM](https://fanatec.com/eu-en/shifters-others/podium-advanced-paddle-module) | ✅ Verified    |
| [Fanatec CSL LC Pedals](https://fanatec.com/eu-en/pedals/csl-elite-pedals) | ✅ Verified    |
| [Fanatec ClubSport Pedals V3](https://fanatec.com/eu-en/pedals/clubsport-pedals-v3) | ✅ Verified    |
| [Fanatec ClubSport Shifter SQ V 1.5](https://fanatec.com/eu-en/shifters-others/clubsport-shifter-sq-v-1.5) | ✅ Verified    |
| [Logitech G29 / G920](https://www.logitechg.com/en-gb/products/driving/driving-force-racing-wheel.html) | ✅ Verified    |
| [PRO Racing Wheel](https://www.logitechg.com/en-gb/products/driving/pro-racing-wheel.html) | 🔲 Untested    |
| [Thrustmaster T300 Racing Wheel](https://eshop.thrustmaster.com/en_us/t300-ferrari-integral-racing-wheel-alcantara-edition.html) | ✅ Verified  |

[comment]: <> (✅ 🔲)


## Environment

This plugin only works on Windows 64 bit.

Latest verified Unity version: 2022.2.1f1

# Notice

Occasionally calls to EnumerateDevices will take orders of magnitude longer than usual to execute (up to 60 seconds), this is caused by a Windows bug attempting to load an absent hardware device. USB Audio DACs & Corsair keyboards are known the cause this issue, try disconnecting and reconnecting offending USB devices. For more information see [this](https://stackoverflow.com/questions/10967795/directinput8-enumdevices-sometimes-painfully-slow) StackOverflow post about the issue from 2012. See issue [#1](/../../issues/1) for more info.

# Support

If you're having any problem, please [raise an issue](https://github.com/MrTimcakes/Unity-DirectInput/issues/new) on GitHub.

# License

This project is free Open-Source software, and is released under the LGPL-3.0 License, further information can be found under the terms specified in the [license](/../../blob/main/LICENSE).
