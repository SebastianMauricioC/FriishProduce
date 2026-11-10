# FriishProduce — Fork

<div align=center><a href=""><img src="https://github.com/CatmanFan/FriishProduce/blob/main/images/icon.png" /></a>

![GBAtemp thread](https://img.shields.io/badge/GBAtemp-thread-blue?link=https%3A%2F%2Fgbatemp.net%2Fthreads%2Ffriishproduce-multiplatform-wad-injector.632028%2F)
 ![Wiki](https://img.shields.io/badge/wiki-white?link=https%3A%2F%2Fcatmanfan.github.io%2FFriishProduce%2F)
</div>

**FriishProduce** is a WAD channel injector/creator for (v)Wii. It can
convert ROMs, disc images, or other types of software into installable WADs
for Wii/vWii (Wii U). This includes injectable Virtual Console (VC) games,
single ROM loaders (SRLs), and Adobe Flash files.

This fork is an independent continuation of
[CatmanFan/FriishProduce](https://github.com/CatmanFan/FriishProduce),
focused on preserving the original functionality while improving
compatibility, online features, and user experience.

> **Notice:** This is not the official upstream repository. Please visit the
> [original project](https://github.com/CatmanFan/FriishProduce) for upstream
> development.

## Features

This injector bypasses other third-party assets, such as Common-Key.bin,
HowardC's tools, and Autoinjectuwad/Devilken's VC, by handling many steps
directly in the program's code.

- Automatic WAD/U8/CCF handling.
- VC ROM injection through hex writing and/or file replacement.
- Automatic banner and icon editing.
- Japanese banner fixes for displaying release year and player count correctly.
- Improved international banner text handling.
- Automatic editing of source WAD save data where available.
- Additional content and emulator options for supported platforms.
- Forwarder creation to auto-load a specific emulator core and ROM.
- Online banner, metadata, and image downloads when public sources are available.
- A localized welcome screen for starting or opening projects.

### Supported platforms

#### Virtual Console

- Nintendo Entertainment System (NES) / Famicom.
- Super Nintendo Entertainment System (SNES) / Super Famicom.
- Nintendo 64.
- SEGA Master System.
- SEGA Mega Drive / Genesis.
- NEC TurboGrafx-16 / PC Engine (HuCARD and CD-ROM).
- SNK NEO-GEO.
- Commodore 64.
- Microsoft MSX / MSX2.

#### Other formats and forwarders

- Adobe Flash.
- Sony PlayStation.
- RPG Maker 2000 / 2003.

Some platforms may require additional resources or may only be partially
implemented. Actual compatibility depends on the ROM, base WAD, emulator, and
hardware being used.

## Wiki

Please check the **[wiki](https://catmanfan.github.io/FriishProduce/)** for a
tutorial on how to use the app and additional tips.

## Building

Requirements:

- Windows 7 or later.
- Visual Studio 2022.
- .NET desktop development workload.
- .NET Framework 4.8 Developer Pack.
- MSBuild and NuGet.

The solution targets .NET Framework 4.8 and uses the `Release|Any CPU`
configuration.

From PowerShell, run:

```powershell
msbuild FriishProduce.sln /t:Build /p:Configuration=Release /p:Platform="Any CPU"
```

The executable is generated at:

```text
FriishProduce\bin\Release\FriishProduce.exe
```

## Fork development

To keep this fork synchronized with the upstream repository:

```powershell
git remote add upstream https://github.com/CatmanFan/FriishProduce.git
git fetch upstream
git checkout main
git merge upstream/main
```

Please do not commit ROMs, WADs containing copyrighted content, BIOS files,
keys, credentials, or other sensitive material.

## Status

This fork is under development. The main workflows compile successfully, but
compatibility should be tested with real ROMs, base WADs, and Wii/vWii hardware
for each platform. A successfully generated file does not guarantee
compatibility with every Wii/vWii revision.

## License

This application is distributed and licensed under the
**GNU General Public License v3.0**
([view in full](https://github.com/CatmanFan/FriishProduce/blob/main/LICENSE)).

This fork retains the original license and copyright notices. Changes made in
this repository are distributed under the same license.

To view the source code for the legacy interface, covering all versions up to
and including **v0.26-beta**, visit
[FriishProduce-Legacy](https://github.com/CatmanFan/FriishProduce-Legacy).

## Credits

- Original project: [CatmanFan/FriishProduce](https://github.com/CatmanFan/FriishProduce).
- Online sources and databases: their respective authors and maintainers.
- Dependencies: their respective projects and licenses.
