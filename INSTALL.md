### [Polytoken](https://docs.polytoken.dev)

#### Install using Git

If you are a Git user, you can install the theme and keep it up to date by cloning the repo:

```bash
git clone https://github.com/dracula/polytoken.git
```

#### Install manually

Download using the [GitHub `.zip` download](https://github.com/dracula/polytoken/archive/main.zip) option and unzip it.

#### Activating theme

1. Copy `dracula.yaml` into your Polytoken themes directory:

   ```bash
   mkdir -p ~/.config/polytoken/themes
   cp dracula.yaml ~/.config/polytoken/themes/dracula.yaml
   ```

   Polytoken stores user themes under `$XDG_CONFIG_HOME/polytoken/themes` (default: `~/.config/polytoken/themes`). If you set `XDG_CONFIG_HOME`, use that path instead.

2. Optionally validate the theme:

   ```bash
   polytoken theme validate ~/.config/polytoken/themes/dracula.yaml
   ```

3. Set the theme in your Polytoken config (`~/.config/polytoken/config.yaml`):

   ```yaml
   tui:
     theme: dark # or `light` for Alucard, or `auto`
     theme-file: $USER_DIRECTORY/themes/dracula.yaml
   ```

   - `tui.theme` picks the palette: `dark` (Dracula), `light` (Alucard), or `auto` (from the terminal background).
   - `tui.theme-file` must be the theme path, including the `.yaml` extension. `$USER_DIRECTORY` resolves to your Polytoken config directory.

   Or preview it for the current session only by running `/theme dracula` inside Polytoken. To confirm Polytoken discovered the file, run `polytoken theme list`.

4. Boom! It's working ✨
