# Hello World NodeMCU external module

This example module demonstrates how to create a basic Lua Module for NodeMCU/ESP32. It exports one function `new()` that returns a greeter helloworld object.

To add to your NodeMCU build, edit/create `extmods.ini` in your repository root as follows: 

```ini
[helloworld]
url=https://github.com/espore-ide/nodemcu-module-helloworld.git
ref=master
```

Then, run `make extmod-update flash`

You will be able to access `helloworld` in lua:

```lua
greeter = helloworld:new("Javier")
greeter:hello("NodeMCU rocks!")
```