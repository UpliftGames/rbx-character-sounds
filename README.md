# rbx-character-sounds
Packaged format of the Roblox RbxCharacterSounds for use with Wally

This repo pulls the RbxCharacterSounds and packages it in a format that is compatible with wally.

The repository is setup to pull the RbxCharacterSounds every 12 hours and update if out of date.

## Package interface

Info on the interface of this package can be found [here](https://github.com/UpliftGames/pull-player-scripts/blob/main/cli/PlayerScripts/RbxCharacterSounds/README.md).

tl;dr:

```Lua
-- returns a copy of the version of the package
Package.getVersionInfo(): {[string]: string}

-- returns the RbxCharacterSounds script
Package.get(): LocalScript

-- returns a copy of the RbxCharacterSounds script
Package.getCopy(): LocalScript

-- replaces the RbxCharacterSounds under StarterPlayer.StarterPlayerScripts 
-- with the provided module script
Package.replace(rbxCharacterSounds: LocalScript)
```

## Where's the source?

The source is currently pulled to the release branch to keep the main branch free of any automated changes.

The only important file in this repo is [release.yml](.github/workflows/release.yml). The heavy lifting is done by this [tool](https://github.com/UpliftGames/pull-player-scripts).
