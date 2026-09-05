# lxorb's Homebrew tap

A [Homebrew](https://brew.sh) tap for macOS.

## Install

```sh
brew install --cask --no-quarantine lxorb/tap/nib
```

`--no-quarantine` is needed because Nib is not notarized by Apple: without it,
Gatekeeper refuses to open the copy Homebrew quarantines. Everything else works
the usual way:

```sh
brew upgrade --cask lxorb/tap/nib   # update
brew uninstall --cask lxorb/tap/nib # remove the app
brew uninstall --zap --cask lxorb/tap/nib # remove the app and its data
```

## Casks

| Cask | Description |
| --- | --- |
| [nib](Casks/nib.rb) | [Nib](https://nibeditor.com) - a simple, lightweight markdown editor offering all the features you could ever need. Universal build, Intel and Apple silicon. |

The cask is bumped automatically by Nib's release pipeline, and `livecheck`
tracks upstream releases:

```sh
brew livecheck --cask lxorb/tap/nib
```
