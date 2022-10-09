# Phi Example Plugin

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Phi is a modular discord bot coded in JavaScript. The following repository contains an example plugin for the Plugin API v2.

## File Structure

The file structure for a Phi plugin looks something like this:

```
phi plugin
↳ .gitignore
↳ config.json
↳ LICENSE
↳ main.js
↳ package.json
↳ README.md
```

* `package.json`: This file contains general information about your plugin and will be used by Phi when loading the plugin.
* `main.js`: This file is the entry point of your plugin. It must follow the specifications below for the main source file.
* `config.json`: The plugins settings are configured with a local config.json rather than Phi's main one.

It is recommended that additional source files for the plugin are placed within a `src` directory.

## Plugin Main Source File

In order to be properly loaded by Phi, the entry point of your plugin must export an object containing all of it's listeners and commands.

```js
// main.js

module.exports = {
    commands: [

    ],
    listeners: [

    ]
}

```

If you want to import the Phi object to have access to the rest of the bot, you can do so with `require('../main')`.

## Configuration

In order to meet Plugin v2 specifications, any configuration should ideally be done with a local `config.json` file instead of Phi's main one.

## Contributors

* [Arisien](https://github.com/Arisien) - Main developer

## License
Phi Example Plugin is licensed under the [MIT](LICENSE) license. Feel free to fork the repository or modify the code as you see fit.