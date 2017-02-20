This repository contains mods for [Stardew Valley](http://stardewvalley.net/) that are maintained
by the community.

## Community mods
The following mods are maintained by the community:

* _TBD_


## FAQs
### What is a 'community mod'?
When a mod is no longer maintained, the author can choose to let the community maintain it. They do
this by releasing the source code, [choosing an open license](https://choosealicense.com/), and
adding Pathoschild as a co-maintainer on the Nexus page.

The mod code is merged into this GitHub repository and kept up-to-date with the latest SMAPI and
Stardew Valley changes. Any developer can submit a pull request to make changes to one of these
mods, and these changes are released periodically.

More importantly, modders can volunteer to become maintainers for one or more mods. Maintainers can
commit directly to the repository and release new versions on the official Nexus page for the mod.

### What does this mean for the original author?
The original author must [choose an open-source license](https://choosealicense.com/) first. They
can retake control of the mod and Nexus page anytime, and release new versions without an open
license. (However, the license can't be revoked for the code they already released under it.) Their
original source code won't be changed, but they're free to merge the community changes into their
code.

The author will always be credited as original author. (Most licenses make that mandatory, too.)

### What are the requirements?
To be accepted as a community mod...

1. The source code must be available under [an open-source license](https://choosealicense.com/).
   The MIT license is preferred.
2. The mod must be abandoned by the original author.
3. The mod must use SMAPI only � no XNB replacement mods (unless it's done through SMAPI).
4. Pathoschild must have co-maintainer access to the official Nexus page.

### How do I become a maintainer?
Pull requests are welcome from anyone, but maintainers should already be active in the modding
community. If you have a few mods under your belt and hang out in [the modding Discord](https://discord.gg/kH55QXP),
just ask and you'll probably be given access.

### How does licensing work?
The mod's source code must be available under [an open-source license](https://choosealicense.com/).
All community changes to the repository (such as this readme) are released under
[the MIT license](LICENSE.txt), and changes to a mod are released under the license specified by its
`LICENSE.txt` file.

## Compiling the mods
Installing stable releases from Nexus Mods is recommended for most users. If you really want to
compile the mod yourself, read on.

These mods use the [crossplatform build config](https://github.com/Pathoschild/Stardew.ModBuildConfig#readme)
so they can be built on Linux, Mac, and Windows without changes. See [the build config documentation](https://github.com/Pathoschild/Stardew.ModBuildConfig#readme)
for troubleshooting.

### Compiling a mod for testing
To compile a mod and add it to your game's `Mods` directory:

1. Rebuild the project in [Visual Studio](https://www.visualstudio.com/vs/community/) or [MonoDevelop](http://www.monodevelop.com/).  
   <small>This will compile the code and package it into the mod directory.</small>
2. Launch the project with debugging.  
   <small>This will start the game through SMAPI and attach the Visual Studio debugger.</small>

### Compiling a mod for release
To package a mod for release:

1. Delete the mod's directory in `Mods`.  
   <small>(This ensures the package is clean and has default configuration.)</small>
2. Recompile the mod per the previous section.
3. Create a zip file of the mod's folder in the `Mods` folder. The zip name should include the
   mod name and version (like `ModName-1.0.zip`).
