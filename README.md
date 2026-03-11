# Dialogue Balancer

**Dialogue Balancer** is a Subtitle Edit plugin that automatically fixes visually unbalanced two-line dialogue subtitles, redistributing text for optimal readability when one dialogue line is significantly longer than the other.

## Background

Professional subtitling guidelines recommend balanced line lengths for two-line subtitles. Channel 4's subtitling guidelines state: *"Where two lines are used, both should be of roughly equal length with the top line the longer."* BBC guidelines emphasise that lines should be broken at logical points, with linguistic and geometric considerations balanced: prioritising readability over arbitrary splitting.  
Finnish subtitling guidelines (Kieliasiantuntijat ry) further specify that when two speakers share a subtitle, each speaker's dialogue should ideally occupy its own line.

This plugin is specifically designed to work with normalized hyphen formatting (where each dialogue line starts with a hyphen). It effectively balances these lines when the visual disparity becomes too great, while ensuring linguistic integrity.

## Features

- **Smart balancing:** merges uneven dialogue lines and finds the optimal midpoint split.
- **Orphaned hyphen prevention:** never leaves a standalone ` -` at the end of the top line.
- **Configurable threshold** (`Fix if line difference exceeds:`) ignores naturally short dialogues where balancing would be unnecessary; default is 22 characters.
- **Persistent settings:** saves threshold value to `DialogueBalancer.xml` in the Subtitle Edit AppData folder between sessions.

## Installation

1. Download `DialogueBalancer.dll` from the [Releases](https://github.com/fyhtma/DialogueBalancer/releases) section.
2. In Subtitle Edit: **File → Open data folder...**
3. Open the `Plugins` folder and place the `.dll` file inside.
4. Restart Subtitle Edit: the tool appears under **Tools → Dialogues - balance short lines...**

## Usage

For optimal results, ensure your dialogue hyphens are normalized before running this plugin. You can use either of these methods:
1. **Built-in Tool:** Go to **Tools → Fix common errors**, select **Fix dash in dialogs**, and set the Style to **Dash second line with space**.
2. **Plugin:** Run the **DialogueOneHyphen** plugin.

Once the formatting is consistent, run **Dialogue Balancer**, review the proposed changes in the list, adjust the threshold if needed, and click OK.

## License

MIT
