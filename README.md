
## 🎈 ⦁ What is it?
A compact, "mobile" Discord for narrow windows. A working port of
<a href="https://github.com/maenDisease/Float">maenDisease/Float</a> (the archived BetterDiscord theme) for the new Discord UI.

- The **channel list** rests as a strip of icons and slides open on hover, pushing the chat right.
- The **member list** (and the DM profile panel) rests as a strip of avatars and slides open on hover, pushing everything left. Nothing reflows: the chat and the message box keep their width and just move.
- **Width presets** at 700 / 500 / 400 / 300 px hide the topic, extra header buttons, composer buttons, the member strip, the channel strip and finally the server list as the window shrinks.
- Small narrow-window fixes: one-line message headers, image viewer buttons at ≤485 px, threads, forums and the Inbox kept inside the window.

---

## ❔ ⦁ What do you need to use it?
- Discord.
- Vencord.
> (IF YOU DON'T HAVE IT, GO GET IT FIRST, DUH)

> Works on its own and on top of <a href="https://github.com/refact0r/system24">system24</a> or <a href="https://github.com/refact0r/midnight-discord">midnight</a>.

## ✅ ⦁ How to use it?
### Turn off the minimum window size:
Vencord → Settings → **Disable minimum window size**.
> Otherwise Discord won't get narrow enough and this whole theme is pointless, duh!

### Put `float.theme.css` in your Vencord themes folder:
Settings → Themes → **Open Themes Folder**, and drop the file in there.

### Enable it:
Settings → Themes, turn Float on and anything should be working.
> If you use another theme, enable Float **after** it.

## 🔧 ⦁ Customizing
Every knob is a variable in the `:root` block at the top of the file, with Float's original names where they still apply:

`--float-sidebar-width` (`48`):  Channel strip width (unitless px), `0` hides it  
`--sidebar-hover-width` (`240px`):  Channel list width when open  
`--slide-window-on-hover` (`1`):  `1` the chat slides right, `0` the list covers it  
`--float-members-width` (`65px`):  Member strip width, `0px` hides it  
`--members-hover-width` (`240px`):  Member list width when open  
`--slide-window-on-members-hover` (`1`):  `1` everything slides left, `0` the list covers the chat  
`--sidebar-hover-delay` / `--members-hover-delay` (`0s`):  How long to rest on a strip before it opens  
`--sidebar-transition-duration` / `--members-transition-duration` (`0.4s`):  Slide speed  
`--guildicon-size` (`48`):  Server icon size  
`--guildlist-collapse` (`0`):  `1` hides the server list behind a hover strip  
`--topic-opacity` (`1`):  Channel topic in the header  
`--toolbar-visibility` (`flex`):  `none` hides the extra header buttons until hovered  
`--textarea-buttons-gif` / `-sticker` / `-gift` (`flex` / `flex` / `none`):  Composer buttons  

The `@media` blocks under the knobs are the width presets. Edit or delete them freely.

> Class names are matched by prefix (`[class^='sidebar_']`), never by Discord's rotating hashes, so the theme survives most Discord updates (most, not all, it's Discord after all). Labels matched by text (GIF, gift) are the English client's.
