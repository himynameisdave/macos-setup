<div align="center" margin="0 auto 20px">
    <h1>macOS Setup</h1>
    <p style="font-style: italic;">💻 Steps I take for setting up a new McBook</p>
</div>

---

When setting up a new MacBook, here is roughly the series of steps / applications I download in order to get the system in an optimal state for me to develop properly.

## Settings

### Trackpad

1. Disable Look up/dictionary click.
1. Enable tab to click.

### Mission Control

1. Disable "Automatically rearrange Spaces based on most recent use"

### Sound

1. Enable "Play feedback when volume is changed"

### a11y

1. Under "Zoom", enable "Use scroll gesture with modifier keys to zoom", setting the key to ^Control.
1. Under "Display", slightly bump the contrast and cursor size (based on displays being used).
1. Under "Mouse & Trackpad", click "Trackpad Options", then enable dragging via three-finger drag.


## Applications

1. [~Spectacle~](https://www.spectacleapp.com/) - _Deprecated_
    - [Rectangle](https://rectangleapp.com/) - Vital app for moving/resizing windows around the screen.
1. [Spark](https://sparkmailapp.com/) - Sexy email client.
1. [VS Code](https://code.visualstudio.com/download) - Prefered code editor.
1. [iTerm2](https://iterm2.com/) - Prefered terminal client.
1. [Insomnia](https://insomnia.rest/) - Tool for testing APIs (REST & GraphQL).
1. [Slack](https://slack.com/downloads/mac) - Slack, for work and fun.
1. [Pock](https://pock.dev/) - App for customizing the macOS Touch Bar.
1. [Amphetamine](https://apps.apple.com/us/app/amphetamine/id937984704?mt=12) - Keep your Mac awake, on demand.
1. [GPG Tools](https://gpgtools.org/) - Manager for GPG keys.
1. [NordVPN](https://apps.apple.com/us/app/vpn-by-nordvpn-web-security/id1116599239?mt=12) - A nice VPN.
1. [Signal](https://signal.org/download/) - For chatting with pals.
1. [Memory Diag](https://apps.apple.com/us/app/memory-diag/id748212890?mt=12) - Helps with memory management.
1. [Monitor Control](https://github.com/MonitorControl/MonitorControl#-monitorcontrol-) - Control external monitor brightness, contrast or volume via keyboard native keys.

## Homebrew & Command Line Tools

[Homebrew](https://brew.sh/) is a must-have for any macOS system. Install it using the following command, then let's install some stuff:

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

1. `brew install ack` - [`ack`](https://beyondgrep.com/) is like `grep`, but much nicer.
1. `sudo easy_install Pygments` - [`Pygments`](https://github.com/dagwieers/pygments) Better syntax highlighting, for [this command](https://github.com/himynameisdave/dotfiles/blob/2ec0e962f276afd59e3329aab75bc7724e585db5/.aliases#L12).
1. `brew install tree` - [`tree`](https://osxdaily.com/2016/09/09/view-folder-tree-terminal-mac-os-tree-equivalent/) is a nice tree view for the current directory.

## Node

Gotta have [NodeJS](https://nodejs.org/en/)! The best way to install and manage it is using Node Version Manager (`nvm`). Install it like so:

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.1/install.sh | bash
```

You can then proceed to install Node. Run `nvm ls-remote` to list remote versions of node versions.

_Note: After installing node, all future versions should be installed using [this commamnd](https://github.com/himynameisdave/dotfiles/blob/2ec0e962f276afd59e3329aab75bc7724e585db5/.functions#L45-L51). This will install the new version, **and** all the globally installed packages._

### Deno

Now that [Deno](https://deno.land/) is stable/v1, install it so that we can use it for new projects moving forward.

```
brew install deno
```

## Dotfiles

Please check out this [dotfiles](https://github.com/himynameisdave/dotfiles) repository for info on the dotfiles. It includes a `.profile`, along with various `.alises` and `.functions` which I usually use. It also includes the [`starship`](https://starship.rs/) configuration I use (see below).

### Starship

Install [`starship`](https://starship.rs/).

```bash
brew install starship
```

This is a handy terminal tool with some neat features. It has its own `starship.toml` config file that you can find in [my dotfiles](https://github.com/himynameisdave/dotfiles).

## VSCode

### Extensions

1. [Atom Keymap](https://github.com/Microsoft/vscode-atom-keybindings) - Inherit a lot of Atom's keymappings.
1. [Atom One Dark Theme](https://github.com/akamud/vscode-theme-onedark) - Nice theme.
1. [Material Icon Theme](https://github.com/PKief/vscode-material-icon-theme) - Better icons, with support for oodles of extensions.
1. [GitLens](https://github.com/eamodio/vscode-gitlens) - Adds lots of built-in git goodies, such as viewing who last edited a line.
1. [Bracket Pair Colorizer](https://github.com/CoenraadS/BracketPair) - Makes matching brackets have the same color, making code blocks easier to see.
1. [ESLint](https://github.com/Microsoft/vscode-eslint) - ESLint in VSCode.
1. [npm Intellisense](https://github.com/ChristianKohler/NpmIntellisense) - Autocompletes npm modules in import statements.
1. [Svelte](https://github.com/UnwrittenFun/svelte-vscode) - Adds Svelte language support.
1. [Svelte Intellisense](https://github.com/ArdenIvanov/svelte-intellisense) - Adds Svelte intellisense support.
1. [ES7 React/Redux Snippets](https://github.com/dsznajder/vscode-es7-javascript-react-snippets) - _Some_ good snippets for React & Redux. Currently looking for a better replacement.
1. [Go](https://github.com/Microsoft/vscode-go) - Adds language support for the [Go language](https://golang.org/) to VS Code.
1. [Chrome Debugger](https://github.com/Microsoft/vscode-chrome-debug) - Debug code running in Google Chrome from VS Code.
1. [Rainbow CSV](https://github.com/mechatroner/vscode_rainbow_csv) - Make CSVs pretty again!
1. [Sort JS Object Keys](https://github.com/SBeator/sort-js-object-keys) - Alphabetize JS object keys.
1. [Markdown Lint](https://github.com/DavidAnson/vscode-markdownlint) - Lint markdown files for common pitfalls.
1. [Indent 4-to-2](https://github.com/compulim/vscode-indent-4to2) - Simplify converting indentation of tab or 4 spaces into 2 spaces.

### Key Mappings

There are a few key mappings which I prefer to set when setting up VS Code. Hit `SHIFT` + `CMD` + `P` to pull up the commands pallet, then select **Preferences: Open Keyboard Shortcuts**.

- **Move Line Down** - `^` + `⌥` + `↓`
- **Move Line Up** - `^` + `⌥` + `↑`

### Font

Use the [Cascadia font](https://github.com/Microsoft/Cascadia-Code) from Microsoft. Download [this `.ttf` file](https://github.com/microsoft/cascadia-code/releases/download/v1911.21/CascadiaMonoPL.ttf), install the font on your Mac by opening the file, and then in VSCode open up the settings UI and add the following as the `font-family`:

```
'Cascadia Mono PL', Menlo, Monaco, 'Courier New', monospace
```

## iTerm

### Colours

Use the [provided colour pallet](https://github.com/himynameisdave/macos-setup/blob/master/himynameisdave.itermcolors). You can add them under **Preferences > Profiles > Colors > Color Presets > Import**.

### Keys

Under **Preferences > Profiles > Keys**, alter the following two key combos:

- `⌥` + ⬅️ - Send Escape Sequence `b`
- `⌥` + ➡ - Send Escape Sequence `f`

### Fonts

In order to use [`starship`](https://starship.rs/), you'll need a [Nerd Font](https://www.nerdfonts.com/) that supports the glyphs to be used in the terminal. I prefer the [`Cascadia` variant](https://github.com/ryanoasis/nerd-fonts/releases/download/v2.1.0/CascadiaCode.zip). You can add it to iTerm via **Profiles > Text**.

---

> _✌️ Made by [Dave](http://himynameisdave.com)._
