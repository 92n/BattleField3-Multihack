# BattleField3-Multihack
[![C++](https://img.shields.io/badge/language-C%2B%2B-%23f34b7d.svg?style=plastic)](https://en.wikipedia.org/wiki/C%2B%2B) 
[![Windows](https://img.shields.io/badge/platform-Windows-0078d7.svg?style=plastic)](https://en.wikipedia.org/wiki/Microsoft_Windows) 
[![x86](https://img.shields.io/badge/arch-x86-red.svg?style=plastic)](https://en.wikipedia.org/wiki/X86) 
[![License](https://img.shields.io/github/license/danielkrupinski/Osiris.svg?style=plastic)](LICENSE)
<br>![Windows](https://github.com/danielkrupinski/Osiris/workflows/Windows/badge.svg?branch=master&event=push)

Free open-source cheat software for the **Battlefield 3** game. Designed as an internal cheat - [Dynamic-link library](https://en.wikipedia.org/wiki/Dynamic-link_library) (DLL) loadable into game process. Compatible with the Originversion of the game.
> Note, this is not fully my source and I do not take credit for the work that's not mine. You can find the source on UC. This is just a fork.
## Features
* **Aimbot** - aim assistance
* **Visuals** - miscellaneous visual options
* **Skin changer** - change weapon skins, knives and stickers
* **Misc** - miscellaneous features

## Getting started

### Prerequisites
Microsoft Visual Studio 2019 (preferably the latest version), platform toolset v142 and Windows SDK 10.0.x.x are required in order to compile Osiris. If you don't have ones, you can download VS [here](https://visualstudio.microsoft.com/) (Windows SDK is installed during Visual Studio Setup).

### Downloading

There is one option of downloading this source.:

#### Without [git](https://git-scm.com)

Choose this option if you want pure source and you're not going to contribute to the repo. Download size ~600 kB.

### Compiling from source

When you have equiped a copy of source code, next step is opening **main.dll** in Microsoft Visual Studio 2019.

Then change build configuration to `Release | x86` and simply press **Build solution**.

If everything went right you should receive `main.dll`  binary file.

### Loading / Injecting into game process

Open your favorite [DLL injector](https://en.wikipedia.org/wiki/DLL_injection) and just inject `main.dll` into `bf3.exe` process.

When injected, menu is openable under `INSERT` key.

### Further optimizations
If your CPU supports AVX / AVX2 / AVX-512 instruction set, you can enable it in project settings. This should result in more performant code, optimized for your CPU. Currently SSE2 instructions are selected in project settings.

## FAQ

### How do I open menu?
Press <kbd>INSERT</kbd> while focused on the Battlefield 3 window.

### What hooking methods this uses?
Currently implemented hooking methods are:
- MinHook - trampoline hook
- VmtHook - hook a function directly in a vtable
- VmtSwap - create a copy of a vtable and swap the pointer on the class instance


This isn't fully my source. Just a few things I wanted to try. Find out yourself.
