# bukkit-runtime

<img src="https://github.com/projopenrealms/brand/blob/master/icon-solid/icon-solid.png" width="200" alt="OpenRealms Logo" />

This is a Bukkit plugin, written in Java, that can execute OpenRealms plugins that are written in JavaScript.

This project implements a JavaScript runtime for running OpenRealms plugins on a Minecraft server. If you're just trying to build a Minecraft plugin using JavaScript, check out [github.com/customrealms/core](https://github.com/customrealms/core).

## How it works

When this plugin is run on a Bukkit-compatible Minecraft server, the plugin launches a V8 JavaScript runtime. Then, it fills that runtime with several globals that allow the JavaScript code to interact with the Minecraft game. Then, finally, it executes the JavaScript code for the OpenRealms plugin.

## JavaScript runtime globals

The JavaScript runtime is populated with several globals. The most basic are `console.log`, `setTimeout`, and a few other related ones. However, the most interesting are related to Minecraft itself.

A few notable globals that are specific to OpenRealms are `Java.resolve`, `BukkitEvents`, and `BukkitCommands`.

The full declaration file for JavaScript globals in OpenRealms is [found here](https://github.com/projopenrealms/core/blob/master/src/globals.ts).

## How does this project relate to [projopenrealms/core](https://github.com/projopenrealms/core)?

This is a Java project that allows you to run JavaScript plugins on a Minecraft server. It implements some bare-bones JavaScript functions, but that's all.

On the other hand, **openrealms/core** is a JavaScript library that picks up where this project leaves off, to make it much easier to build Minecraft plugins. It basically just provides some developer-friendly utilities.

You can create OpenRealms plugins without **openrealms/core**, but you'll find it's much more tedious.

## Contributing

We need your help to solve bugs, implement new features, and optimize the entire system. If you want to help, please join our [Discord](https://discord.com/invite/bbS2ACdTCM) and/or check out the [Issues tab](https://github.com/projopenrealms/bukkit-runtime/issues).
