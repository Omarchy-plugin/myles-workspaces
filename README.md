# myles.workspaces

Workspace number indicators for the Omarchy bar.

> **Derived work.** Forked from Omarchy's built-in `omarchy.workspaces` and substantially modified.
> See [Credits](#credits) for licensing.

A bar widget that shows workspace number indicators.

## What it does

Renders the active Hyprland workspace set and lets you switch by clicking an indicator.
Visual behaviour matches Omarchy's built-in workspaces widget.

## Requirements

Hyprland only — the widget talks to the compositor's IPC socket. No extra packages, no
network calls, no external scripts.

## Install

```bash
omarchy plugin add https://github.com/Omarchy-plugin/myles-workspaces.git --enable --yes
```

That clones, validates, installs to `~/.config/omarchy/plugins/myles.workspaces/`, and places it on your bar.

The stock `omarchy.workspaces` widget does the same job and will fight with this one. Turn it off:

```bash
omarchy plugin disable omarchy.workspaces
```

## Update

```bash
omarchy plugin update myles.workspaces --yes
```

Or update every git-managed plugin at once:

```bash
omarchy plugin update --yes
```

## Uninstall

omarchy plugin enable omarchy.workspaces   # if you want the built-in back

omarchy plugin remove myles.workspaces --yes

## Installing the whole suite

Every plugin in the suite installs with one command, and updates itself
automatically:

```bash
git clone https://github.com/Omarchy-plugin/myles-omarchy-plugins.git
cd myles-omarchy-plugins && ./install.sh
```

See [myles-omarchy-plugins](../myles-omarchy-plugins) for the update mechanism.

## Credits

- Omarchy — <https://omarchy.org> — MIT, © David Heinemeier Hansson. `omarchy.workspaces` is the base this is forked from.
- Mylesoft — <https://github.com/Omarchy-plugin> — modifications.

Plugins run unsandboxed inside the long-lived `omarchy-shell` process with your user
permissions. Review the source before enabling anything you did not write.
