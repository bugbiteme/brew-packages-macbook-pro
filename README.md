# brew-packages-macbook-pro
List of packages installed on macbook with homebrew

## Install 

On the new Mac, ensure that Homebrew is installed. Then, you can use the following commands to install everything from the lists:

For formula:

```
xargs brew install < brew-formula-list.txt
```

For casks:

```
xargs brew install --cask < brew-cask-list.txt
```

This method allows you to easily export and re-install all the apps and utilities you have installed via Homebrew on another Mac.

## Uninstall

To use the exported list to uninstall packages from a Mac, you can follow a similar process, but with the brew uninstall command instead.

Here’s how you can do it:

### Uninstall packages:

If you have a brew-formula-list.txt file with the list of installed formula, you can run:

```
xargs brew uninstall < brew-uninstall.txt
```

This will uninstall all the formulae listed in the `brew-uninstall.txt` file.

## Exporting from an existing Mac

To export the list of applications installed via Homebrew and Homebrew Cask and use it for installing them on another Mac, follow these steps:

### Export the list of installed formula and casks:

Use the following commands to generate a list of the installed formulae (regular packages) and casks (macOS applications) and export them to a file.

```
brew list --formula > brew-formula-list.txt
brew list --cask > brew-cask-list.txt
```

This will create two files: `brew-formula-list.txt` (for the formula) and `brew-cask-list.txt` (for the casks).