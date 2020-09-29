# native-redirect
Compatibility tool for running native versions of titles that only have Windows versions available on Steam.

### What does it do?
Runs user provided native Linux binaries for a game using the Steam Runtime, providing play time tracking. Useful for games that got official Linux support outside of Steam, or community source ports (Unreal Tournament, Quake III Arena, the original Prey).

### What does it NOT do?
Steamworks features like achievements will not work. None of the games I tested had that in their Windows versions, so probably not a big deal.

### Installation and use
1. Unpack `native-redirect` to `~/.steam/root/compatibilitytools.d`
2. Restart Steam (if it was already running)
3. Navigate to the game's install folder and install the Linux binaries you have acquired for the game like normal
4. Create a script called `_play.sh` in the same folder as the Windows executable Steam uses to run the game. The job of this script is simply to execute your Linux binary
5. Force the use of the "native-redirect" compatibility tool in the game's "Properties" dialog in Steam.

### Some gotcha's
This compatibility tool runs your game using the Steam runtime. There may be libraries provided by your distro that are not provided by the Steam runtime. Running Steam from a console will allow you to see error messages when trying to boot a game. Missing libraries mentioned can be placed next to the binary being executed.
