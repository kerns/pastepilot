# PastePilot X for Visual Studio Code

PastePilot X is an extension for Visual Studio Code that allows you to combine multiple files into a single, easy-to-read block of text. Additionally, it can generate an ASCII tree view of your project, which can also be included in the final output. The goal of PastePilot X is to create a contextually rich blob of text, easily understood by both humans and artificial intelligence alike.

To use it simply select multiple files in the Visual Studio Code explorer sidebar and right-click on one of the selected files. Choose "PastePilot X" from the context menu and the concatenated content will be copied to your clipboard.

## Features

- Concatenate multiple selected files into a single, structured text.
- Optionally prepends an ASCII tree of your project's folder structure.
- Wraps each file's content with custom comments indicating the beginning and end of each file.
- Local configuration support with optional `.pastepilot.config.js` file.

## Installation

1. Open Visual Studio Code.
2. Open the command palette (Mac: `Cmd+P` / Win: `Ctrl+P`) and type `ext install kerns.pastepilot-x` and press `Enter`, or search for "PastePilot X" in the extensions tab.
3. Restart Visual Studio Code.

## Usage

1. In the Visual Studio Code explorer sidebar, select multiple files while holding down `Ctrl` (Windows) or `Cmd` (Mac).
2. Right-click on one of the selected files and choose "PastePilot X" from the context menu.
3. The concatenated content, along with the ASCII tree (if enabled), will be copied to your clipboard.

## Configuration

Global settings can be configured in Visual Studio Code's settings, under the "PastePilot X" section. If you need them, local settings can be configured to override global settings on a per-project basis by way of a `.pastepilot.config.js` placed on the root of your project.

The following settings can be configured:

- `asciiTreePrepend`: Whether to prepend an ASCII tree of the project's folder structure
- `asciiTreeMaxDepth`: Maximum depth for the ASCII tree
- `ignoreFile`: File to use for ignoring folders in the ASCII tree (defaults to `.gitignore`)
- `prependComment`: Comment to prepend before each file's content
- `appendComment`: Comment to append after each file's content

A sample `.pastepilot.config.js` file might look like this:

```javascript
module.exports = {
  asciiTreePrepend: true,
  asciiTreeMaxDepth: 3,
  ignoreFile: ".customignore",
  prependComment: "/* Begin custom $path */",
  appendComment: "/* End custom $path */",
};
```

Changes to your `.pastepilot.config.js` configuration file require a restart.

## Feedback

Bugs, ideas, feedback and pull requests are welcome. Please use the [GitHub issue tracker](https://github.com/kerns/pastepilot/issues)
