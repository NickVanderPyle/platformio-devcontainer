# PlatformIO Devcontainer

## [devcontainer.json](./.devcontainer/devcontainer.json)

* Adds PlatformIO extension for VSCode
* Exposes port 8008 so that PIO Home isn't blank when opening a PIO Home tab in VSCode
* Mounts /dev so that Arduino devices on USB can read and written to
* Not sure `--privileged` is still necessary

## [Dockerfile](./.devcontainer/Dockerfile)

* Installs Python and Clang dependencies
* Sets udev rules to allow non-root to write to arduino devices in /dev
* Sets a non-root user
* Installs PlatformIO CLI tools

## [settings.json](./.vscode/settings.json)

* Sets the PIO Home port to 8008 which is the port that's exposed in [devcontainer.json](./.devcontainer/devcontainer.json)