nvmw-fix [![npm](https://img.shields.io/npm/v/nvmw-fix.svg?style=plastic)](https://npmjs.org/package/nvmw-fix) [![npm](https://img.shields.io/npm/dm/nvmw-fix.svg?style=plastic)](https://npmjs.org/package/nvmw-fix)
====

- [简体中文](README_zh.md) &#8195;&#8195; [English](README_en.md)

The following is from the machine, if there is a mistake, please understand

This tool provides a straightforward method for switching global Node.js versions without the need to configure environment variables or obtain administrative privileges.   Simply installing the npm package allows for its use via command line.

Application scenario: In environments where software installation is restricted, such as in certain corporate settings, this tool remains effective as it only requires the installation of an npm package.


## Installation

```shell
npm i -g nvmw-fix
```

## Usage

```shell

// Open the command line terminal

// View the Node.js version currently in use
node -v 

// list the installed all Nodes
nvmw ls

// install the given version of Node
nvmw install  v22.13.0

// permanently use the given version of Node as default
nvmw switch  v22.13.0

// Close this command line terminal, open a new command line terminal, and view the current version of Node.js
node -v

// output v22.13.0，it works
```

All commands are listed as follows:

```shell

nvmw -h

  Usage: nvmw [options] [command]

  Commands:

    install <version>      install the given version of Node
    uninstall <version>    uninstall the given version of Node
    use <version>          use the given version of Node in current shell
    deactivate             undo effects of nvmw in current shell
    switch <version>       permanently use the given version of Node as default
    switch-deactivate      permanently undo effects of nvmw
    ls                     list the installed all Nodes
    ls-remote              list remote versions available for install
    cleanup                remove stale local caches

  Options:

    -h, --help     output usage information
    -V, --version  output the version number

```

## Notes

* It only works in Windows CMD.
* This tool can't install the Node which version below v4.5.0.
* You should install a system version Node with [Windows installer](https://nodejs.org/en/download/).
* fork from  [nvmw](https://github.com/nanjingboy/nvmw) to fix bug, if you previously used nvmw, please uninstall it global before use

```shell
npm uninstall -g nvmw
```

## License
[MIT](http://www.opensource.org/licenses/MIT)
