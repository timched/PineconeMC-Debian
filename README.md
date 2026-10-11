# PineconeMC (FireyTech fork)

> [!NOTE]
> This is a **fork of [PineconeMC](https://github.com/ElyPrismLauncher/Launcher)**, which is itself a fork of [Prism Launcher](https://prismlauncher.org). This fork only ships **`.deb` packages**. There are no AppImage, Flatpak, Windows, or macOS builds here.

<p align="center">
  A fork of PineconeMC that adds integrated support for Ely.by accounts (MSA accounts can still be used)<br />
  <br />This is <b>not</b> endorsed by Prism Launcher, PineconeMC, or Ely.by.
</p>

## Features

Inherited from PineconeMC:

- **Ely.by login via OAuth2.** Your credentials never touch the launcher. You log in on the official Ely.by page in your browser, and Ely.by gives the launcher a limited-privilege token.
- **Skins on any server.** Uses Ely.by's official Authlib patches rather than relying only on authlib-injector, so skins show up even on servers without a skins plugin.
- **Microsoft accounts still work.**

## Installation

Only `.deb` packages are provided. Download the latest one from the [Releases](https://github.com/<your-username>/<your-repo>/releases/latest) page, then install it from the folder where you saved it:

```bash
cd ~/Downloads
sudo apt install ./pineconemc_*.deb
```

Using `apt install ./file.deb` (instead of `dpkg -i`) also pulls in any missing dependencies.

## Downloads and Verification

> [!CAUTION]
> Malicious copies of PineconeMC have been spotted in the wild. Only download this fork from the official Releases page of this repository. Do not trust links from other sources.

## Development Builds

Development builds are not intended for most users. They may be unstable, and their binaries include debug information, so the files are larger.

## Building

To build the `.deb` yourself, follow the [Prism Launcher build instructions](https://prismlauncher.org/wiki/development/build-instructions), then package the result with your own `.deb` tooling.

## Community & Support

Open a GitHub issue if you find a bug or want a feature. (only on the official repo) For upstream support, see the [PineconeMC Discord](https://discord.gg/5kcBCvnbTp).

## Licensing and Attribution

This project is a fork of PineconeMC and Prism Launcher. It is not affiliated with or endorsed by either project, or by Ely.by.

All launcher code is licensed under **GPL-3.0-only**. The logo and related assets are under **CC BY-SA 4.0**.

### Forking / Redistribution

If you fork this project or build custom versions, please:

- Make it clear that your fork is not Prism Launcher, PineconeMC, or endorsed by either project.
- Replace the API keys in [CMakeLists.txt](CMakeLists.txt) with your own, or set them to empty strings (`""`) to disable the features that need them.

Building without removing the provided API keys means you accept the [Microsoft Identity Platform Terms of Use](https://docs.microsoft.com/en-us/legal/microsoft-identity-platform/terms-of-use) and the [CurseForge 3rd Party API Terms](https://support.curseforge.com/en/support/solutions/articles/9000207405-curse-forge-3rd-party-api-terms-and-conditions).
