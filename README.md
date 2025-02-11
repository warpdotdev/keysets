# Warp Keyboard Shortcut Presets

This is an open source repository with custom keyboard shortcut presets for
[Warp](https://www.warp.dev).

## Installation

### Disclaimer

These presets are a work in progress and may be missing some functionality. As we continue to
improve Warp and support more behaviors, they will be updated. If you have any questions or run into
any issues, please reach out to us either on [Discord](https://discord.gg/warpdotdev) or in our
[Issues Repository](https://github.com/warpdotdev/Warp)

### How to Install on Mac or Linux

To use any of these keyboard presets, follow these steps:

1. Confirm that you have a `~/.warp` directory. If you don't, create it with `mkdir ~/.warp`
2. If you have an existing `keybindings.yaml` file, back it up by renaming it to
   `keybindings.yaml.bak`
3. Copy the appropriate `.yaml` file from this repo into `~/.warp/`
4. Rename that file to `keybindings.yaml`
5. Restart Warp

### How to Install on Windows

To use any of these keyboard presets, follow these steps:

1. Confirm that you have a `$env:LOCALAPPDATA\warp\Warp\config\` directory. If you don't, create it with `mkdir $env:LOCALAPPDATA\warp\Warp\config\`
2. If you have an existing `keybindings.yaml` file, back it up by renaming it to
   `keybindings.yaml.bak`
3. Copy the appropriate `.yaml` file from this repo into `$env:LOCALAPPDATA\warp\Warp\config\`
4. Rename that file to `keybindings.yaml`
5. Restart Warp

That's it! When Warp re-opens it will pick up your new keyboard shortcuts and automatically apply
them. Any additional customizations you make to your keybindings will also be saved into
`keybindings.yaml`, so feel free to modify them as you see fit.

## Uninstallation

If you decide that you don't like a preset and want to restore your previous settings, follow these
steps:

1. Delete `keybindings.yaml`
2. Rename the back-up you created in step (2) above back to `keybindings.yaml`
3. Restart Warp

## Contribution

We welcome and appreciate any contributions! The existing preset files should serve as an example
for the format, however a more comprehensive description of the file format is available in
[FORMAT.md](FORMAT.md)
