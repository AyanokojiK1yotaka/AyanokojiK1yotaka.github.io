# Nikhil.OS

My personal homepage, designed to look and feel like a tiny retro operating system.

**Live site: [ayanokojik1yotaka.github.io](https://ayanokojik1yotaka.github.io/)**

<img width="1080" height="1350" alt="nikhil-os-thumbnail" src="https://github.com/user-attachments/assets/fb37181d-a9e2-4c4d-89f8-ea3a355e3259" />

Drag the windows, type commands in the terminal, press `Ctrl+K` to jump anywhere,
and slide the numbers on the compounding calculator.

## Features

- **Retro desktop UI** with draggable windows, a menu bar and a taskbar that shows which windows are open
- **Boot screen** on the first visit of a session (any key or tap skips it; it is turned off for reduced-motion users)
- **Launcher** (`Ctrl+K`, `Cmd+K` or `/`) to open any window or run an action by typing
- **Working terminal** with tab completion and command history
- **Sound effects**: clicks, typing ticks, window open/close, themes and a few surprises, all synthesised in the browser with the Web Audio API, so there are no audio files to download. They are on by default and start after a visitor's first click or key press (browsers block audio before that). Mute with the ♪ button, `sound off` in the terminal, or the launcher; the choice is remembered
- **Four themes** (`teal`, `plum`, `graphite`, `classic`), plus a switch for the CRT scanlines
- **Machine learning toy**: click to add points and a line fits them live, with an R² score
- **Compounding calculator**: monthly amount, years and yearly return, with a year-by-year chart
- **Live projects**: the Projects window lists my latest public GitHub repos (it falls back to placeholders if there are none)
- A few easter eggs. Try `help` in the terminal and poke around.

## Terminal commands

| Command | What it does |
| --- | --- |
| `help` | List the available commands |
| `open <window>` | Open a window (`about`, `ml`, `finance`, `projects`, `tools`, `contact`) |
| `theme [name]` | Cycle themes, or pick one by name |
| `neofetch`, `stack`, `whoami`, `ls` | Quick facts about me and this site |
| `email` | Copy my email address |
| `crt` | Toggle the scanlines |
| `sound [on\|off]` | Toggle sound effects |
| `uptime`, `date`, `history`, `echo`, `clear` | The usual |
| `reboot` | Replay the boot sequence |

## Tech

Everything is in a single `index.html`: plain HTML, CSS and JavaScript with no build step,
framework or dependencies. The pixel font is [VT323](https://fonts.google.com/specimen/VT323)
(SIL Open Font License), loaded from Google Fonts.

Also included:

- Keyboard and screen-reader support: skip link, labelled controls and `aria-live` status updates
- `prefers-reduced-motion` support
- A print stylesheet
- Open Graph and Twitter Card metadata with `og-image.png` for link previews, plus structured data

## Run it locally

```bash
git clone https://github.com/AyanokojiK1yotaka/AyanokojiK1yotaka.github.io.git
cd AyanokojiK1yotaka.github.io
python3 -m http.server 8000
```

Then open <http://localhost:8000>. Serving it over HTTP (rather than opening the file directly)
lets the live GitHub repo list work.

## Deploy

This repo is a GitHub Pages user site. Pushing to the default branch publishes it at
`https://<username>.github.io/`.

## Make it yours

If you fork it, these are the places to edit in `index.html`:

- **Text and links**: the window contents, the GitHub, LinkedIn and X links, and the `mailto:` address
- **Colours**: the CSS variables at the top of the stylesheet, and the theme blocks that follow
- **GitHub username**: search for `api.github.com/users/` in the script to change which repos are listed
- **Metadata**: the `<title>`, description, Open Graph tags, canonical URL and the JSON-LD block in `<head>`

## Privacy

No analytics, trackers or cookies. The browser's `localStorage` and `sessionStorage` are used only for small
preferences (theme, scanlines, sound on/off, whether the boot screen has played) and the "visit no." counter,
which counts visits in your own browser, not across all visitors.

## Contact

[LinkedIn](https://www.linkedin.com/in/nikhil-gowda-69os) · [X](https://x.com/Nikh1lGowda) · [GitHub](https://github.com/AyanokojiK1yotaka)
