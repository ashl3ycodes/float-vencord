# Float for Vencord

A compact, "mobile" Discord for narrow windows. A working 2025-UI port of
[maenDisease/Float](https://github.com/maenDisease/Float), the archived BetterDiscord theme.

- The **channel list** rests as a strip of icons and slides open on hover, pushing the chat right.
- The **member list** (and the DM profile panel) rests as a strip of avatars and slides open on
  hover, pushing everything left. Nothing reflows: the chat and the message box keep their width
  and just move.
- **Width presets** at 700 / 500 / 400 / 300 px hide the topic, extra header buttons, composer
  buttons, the member strip, the channel strip and finally the server list as the window shrinks.
- Small narrow-window fixes: one-line message headers, image viewer buttons at ≤485 px, threads,
  forums and the Inbox kept inside the window.

Works on its own and on top of [system24](https://github.com/refact0r/system24) /
[midnight](https://github.com/refact0r/midnight-discord).

## Install

1. Vencord → Settings → **Disable minimum window size** (otherwise Discord won't get narrow enough).
2. Put `float.theme.css` in your Vencord themes folder (Settings → Themes → **Open Themes Folder**).
3. Enable it under Settings → Themes. If you use another theme, enable Float **after** it.

## Customise

Every knob is a variable in the `:root` block at the top of the file, with Float's original
names where they still apply:

| Knob | Default | What it does |
|---|---|---|
| `--float-sidebar-width` | `48` | channel strip width (unitless px), `0` hides it |
| `--sidebar-hover-width` | `240px` | channel list width when open |
| `--slide-window-on-hover` | `1` | `1` the chat slides right, `0` the list covers it |
| `--float-members-width` | `65px` | member strip width, `0px` hides it |
| `--members-hover-width` | `240px` | member list width when open |
| `--slide-window-on-members-hover` | `1` | `1` everything slides left, `0` the list covers the chat |
| `--sidebar-hover-delay` / `--members-hover-delay` | `0s` | how long to rest on a strip before it opens |
| `--sidebar-transition-duration` / `--members-transition-duration` | `0.4s` | slide speed |
| `--guildicon-size` | `48` | server icon size |
| `--guildlist-collapse` | `0` | `1` hides the server list behind a hover strip |
| `--topic-opacity` | `1` | channel topic in the header |
| `--toolbar-visibility` | `flex` | `none` hides extra header buttons until hovered |
| `--textarea-buttons-gif` / `-sticker` / `-gift` | `flex` / `flex` / `none` | composer buttons |

The `@media` blocks under the knobs are the width presets. Edit or delete them freely.

Class names are matched by prefix (`[class^='sidebar_']`), never by Discord's rotating hashes,
so the theme survives most Discord updates. Labels matched by text (GIF, gift) are the English
client's.

## Credits

Original Float by [maenDisease](https://github.com/maenDisease). This is a rewrite for the new
Discord UI, not a copy of its code; the idea, the behaviour and the knob names are theirs.

See also [float-spicetify](https://github.com/ashl3ycodes/float-spicetify), the same thing for Spotify.

## License

[AGPL-3.0](LICENSE)
