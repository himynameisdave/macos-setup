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

### a11y

1. Under "Zoom", enable "Use scroll gesture with modifier keys to zoom", setting the key to ^Control.
1. Under "Display", slightly bump the contrast and cursor size (based on displays being used).
1. Under "Mouse & Trackpad", click "Trackpad Options", then enable dragging via three-finger drag.


## Applications

1. [Spectacle](https://www.spectacleapp.com/) - Vital app for moving/resizing windows around the screen.
1. [Spark](https://sparkmailapp.com/) - Sexy email client.
1. [VS Code](https://code.visualstudio.com/download) - Prefered code editor.
1. [iTerm2](https://iterm2.com/) - Prefered terminal client.
1. [Insomnia](https://insomnia.rest/) - Tool for testing APIs (REST & GraphQL).
1. [Slack](https://slack.com/downloads/mac) - Slack, for work and fun.
1. [Pock](https://pock.dev/) - App for customizing the macOS Touch Bar.


## Dotfiles

Please check out this [dotfiles](https://github.com/himynameisdave/dotfiles) repository for info on the dotfiles. It includes a `.profile`, along with various `.alises` and `.functions` which I usually use.


## VSCode

### Extensions

1. [Atom Keymap](https://github.com/Microsoft/vscode-atom-keybindings) - Inherit a lot of Atom's keymappings.
1. [Atom One Dark Theme](https://github.com/akamud/vscode-theme-onedark) - Nice theme.
1. [Material Icon Theme](https://github.com/PKief/vscode-material-icon-theme) - Better icons, with support for oodles of extensions.
1. [GitLens](https://github.com/eamodio/vscode-gitlens) - Adds lots of built-in git goodies, such as viewing who last edited a line.
1. [ES7 React/Redux Snippets](https://github.com/dsznajder/vscode-es7-javascript-react-snippets)

### Key Mappings

There are a few key mappings which I prefer to set when setting up VS Code. Hit `SHIFT` + `CMD` + `P` to pull up the commands pallet, then select **Preferences: Open Keyboard Shortcuts**.

- **Move Line Down** - `^` + `⌥` + `↓`
- **Move Line Up** - `^` + `⌥` + `↑`


## iTerm

### Colors

Use the [provided colour pallet](https://github.com/himynameisdave/macos-setup/blob/master/himynameisdave.itermcolors). You can add them under **Preferences > Profiles > Colors > Color Presets > Import**.

### Keys

Under **Preferences > Profiles > Keys**, alter the following two key combos:

- `⌥` + ⬅️ - Send Escape Sequence `b`
- `⌥` + ➡ - Send Escape Sequence `f`

---

> _✌️ Made by [Dave](http://himynameisdave.com)._
