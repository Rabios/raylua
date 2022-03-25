<div align="center">
	<img src="https://github.com/Rabios/raylua/blob/master/raylua.png?raw=true">
	<p>Cross-Platform, Modern, Handwritten, Updated LuaJIT bindings for raylib library.</p>
</div>

### Contains

1. raylib
2. RLGL
3. raylib easings (easings.h)
4. rlights (raylib.lights)
5. raymath
6. physac
7. raygui

> NOTE: You need to build shared lib of physac and raygui.

### Supports

1. Microsoft Windows (32-bit and 64-bit)
2. Mac (64-bit)
3. Linux (64-bit)
4. Android (ARM64)

### Example

Link `raylib.lua` (Via require or dofile), Then start coding!

```lua
local rl = require("raylib")

local screenWidth = 800
local screenHeight = 450

rl.InitWindow(screenWidth, screenHeight, "raylib [core] example - basic window")
rl.SetTargetFPS(60)

while not rl.WindowShouldClose() do
  rl.BeginDrawing()
  rl.ClearBackground(rl.RAYWHITE)
  rl.DrawText("Congrats! You created your first window!", 190, 200, 20, rl.LIGHTGRAY)
  rl.EndDrawing()
end

rl.CloseWindow()
```

For examples that binded see [here](https://github.com/Rabios/raylua/blob/master/examples/README.md)

> All contained functions and variables called from `rl` namespace/table.

### NOTES

1. This is a direct bindings of the original C version, It implements the same content.
2. Hacks and fallbacks of raylib 2 implemented from original C version, raylib 2 functions will still works if you use raylib 3.

> And i didn't copy-pasted from any gist, Even that gist made by Alexander Matz, All bindings were written by me.

### Compatibility

See [`compatibility.md`](https://github.com/Rabios/raylua/blob/master/compatibility.md) for info about this.

### Autocompletion

I finally did autocompletion for raylib Lua/LuaJIT bindings to use in ZeroBrane Studio,See [here](https://github.com/Rabios/raylua/blob/master/zerobrane/README.md) about that and how to use it.

### Using this on cherry

raylua is also available as package for [cherry](https://github.com/Rabios/cherry), And it's easy to install and setup!

```
cherry new D:\cherry-raylua-game
cherry add Rabios/raylua D:\cherry-raylua-game
```

Then edit main file of package in directory `D:\cherry-raylua-game` and require `raylib` with writing game code!

### Running and installing this on LPM

raylua is also available as a package for [LPM](https://lpm.yaumama.repl.co). To setup, install, and run it just use this command:

```
lpm install raylua
```

and to run:
```
lpm jitrun main.lua
```

Replace main.lua with your main file.

### Running this on PUC-RIO Lua (Not LuaJIT)

If you use PUC-RIO Lua (Not LuaJIT), You have to install luaffi rock with luarocks!

Using `luarocks install --server=https://luarocks.org/dev luaffi` command.

However, I don't guarantee that it works same as LuaJIT FFI.

### TSnake41's version

I did custom version using [TSnake41's raylib-lua](https://github.com/TSnake41/raylib-lua), Currently works only on 64-bit versions of Microsoft Windows and 64-bit versions of LuaJIT.

To get it see [tsnake41-raylib-lua](https://github.com/Rabios/raylua/blob/master/tsnake41-raylib-lua) folder.

### Special thanks

1. [Ramon Santamaria (@raysan5)](https://github.com/raysan5), Who created [raylib](https://www.raylib.com).
2. [Astie Teddy (@TSnake41)](https://github.com/TSnake41), Cause my bindings inspired by [his bindings](https://github.com/TSnake41/raylib-lua).
3. [Alexander Matz (@alexander-matz)](https://github.com/alexander-matz), Cause [his gist](https://gist.github.com/alexander-matz/f8ee4eb9fdf676203d70c1e5e329a6ec) was the first reason to write my own bindings from zero.

### License

See [`LICENSE.txt`](https://github.com/Rabios/raylua/blob/master/LICENSE.txt) for bindings license and [`LICENSES.txt`](https://github.com/Rabios/raylua/blob/master/LICENSES.txt) for third party licenses.
