<!-- Screenshot -->
<div align="center">
    <img src="https://awesomewm.org/images/awesome-logo.svg">
</div>

<br>

<div align="center">
    <img src="assets/awesome.png">
</div>

<br>
<br>

<a href="https://awesomewm.org/"><img alt="AwesomeWM Logo" height="160" align = "left" src="https://awesomewm.org/doc/api/images/AUTOGEN_wibox_logo_logo_and_name.svg"></a>
<b> AwesomeWM Dotfiles </b>

Welcome to my AwesomeWM configuration files!

so yeah now i'm using awesomewm, looks like i'll be use this wm forever.

Because only this wm can satisfy me.

Fyi, I use night colorscheme, and it's so beautiful.

These dotfiles are made with love, for sure.

<h2></h2><br>

**Here are some details about my setup:**

| Programs   | Using       |
| ---------- | ----------- |
| WM         | awesome-git |
| OS         | arch linux  |
| Terminal   | kitty       |
| Shell      | zsh         |
| Editor     | neovim      |
| Compositor | picom       |
| Launcher   | rofi        |
| Browser    | firefox     |

<h2></h2><br>

<details open>
<summary><strong>S E T U P</strong></summary>

1. Install dependencies and enable services

   - Dependencies

     - **Arch Linux** (and all Arch-based distributions)

       _Assuming your AUR helper is_ `paru`

       ```shell
       paru -S awesome-git picom-git kitty rofi todo-bin acpi acpid \
       wireless_tools jq inotify-tools polkit-gnome xdotool xclip maim \
       brightnessctl alsa-utils alsa-tools pulseaudio lm_sensors \
       mpd mpc mpdris2 ncmpcpp playerctl lsd bat fzf zsh htop neofetch \
       gpick libnotify xdg-user-dirs firefox unzip --needed
       ```

   - Services

     ```shell
     # For automatically launching mpd on login
     systemctl --user enable mpd.service
     systemctl --user start mpd.service
     # For charger plug/unplug events (if you have a battery)
     sudo systemctl enable acpid.service
     sudo systemctl start acpid.service
     ```

2. Install needed fonts

   Copy the required fonts inside the `misc/fonts` folder of this repository.

   ```sh
   cp -r ./misc/fonts/* ~/.fonts/
   # or to ~/.local/share/fonts
   cp -r ./misc/fonts/* ~/.local/share/fonts/
   ```

   And run this command for your system to detect the newly installed fonts.

   ```sh
   fc-cache -fv
   ```

3. Install my AwesomeWM configuration files

   > Clone this repository

   ```shell
   git clone https://github.com/rojasricor/AwesomeWMDotfiles.git
   cd AwesomeWMDotfiles
   ```

   > Copy config and binaries files

   ```shell
    cp -r ./config/* ~/.config/
    cp -r ./bin/* ~/.local/bin/
    cp -r ./misc/.* ~/
   ```

4. Configure stuff

   The relevant files are inside your `~/.config/awesome` directory.

   - User preferences and default applications

     In `rc.lua` there is a _Default Applications_ section where user preferences and default applications are defined.
     You should change those to your liking.

     Note: For the weather widgets to work, you will also need to create an account on [openweathermap](https://openweathermap.org), get your key, look for your city ID, and set `openweathermap_key` and `openweathermap_city_id` accordingly.

5. Lastly, log out from your current desktop session and log in into AwesomeWM.

</details>

<br>

<details open>
<summary><strong>F E A T U R E S</strong></summary>

<b>These are the features included in my AwesomeWM setups!</b>

- Aesthetic `Dashboard` ngl.
- Notification Center
- Control Panel
- ToDo Reminder
- Battery Indicator
- PopUp Notifications
- Applications Launcher
- Custom mouse-friendly `ncmpcpp` UI with album art ofc.
- Word Clock Lockscreen with PAM Integration
- Some Tooltip Widget
- Hardware Monitor
- Beautiful `colorscheme` ikr, named `night` and created by [ner0z](https://github.com/ner0z)

</details>

<br>

<details open>
<summary><strong>K E Y B I N D S</strong></summary>

I use <kbd>super</kbd> AKA Windows key as my main modifier.
also with <kbd>alt, shift, and ctrl</kbd>

**Keyboard**

| Keybind                          | Action                                               |
| -------------------------------- | ---------------------------------------------------- |
| <kbd>super + enter</kbd>         | Spawn terminal                                       |
| <kbd>super + w</kbd>             | Spawn web browser                                    |
| <kbd>super + x</kbd>             | Spawn color picker                                   |
| <kbd>super + f</kbd>             | Spawn file manager                                   |
| <kbd>super + d</kbd>             | Launch applications launcher                         |
| <kbd>super + shift + d</kbd>     | Toggle dashboard                                     |
| <kbd>super + q</kbd>             | Close client                                         |
| <kbd>super + ctrl + l</kbd>      | Toggle lock screen                                   |
| <kbd>super + [1-0]</kbd>         | View tag AKA change workspace (for you i3/bsp folks) |
| <kbd>super + shift + [1-0]</kbd> | Move focused client to tag                           |
| <kbd>super + space</kbd>         | Select next layout                                   |
| <kbd>super + s</kbd>             | Set tiling layout                                    |
| <kbd>super + shift + s</kbd>     | Set floating layout                                  |
| <kbd>super + c</kbd>             | Center floating client                               |
| <kbd>super + [arrow keys]</kbd>  | Change focus by direction                            |
| <kbd>super + shift + f</kbd>     | Toggle fullscreen                                    |
| <kbd>super + m</kbd>             | Toggle maximize                                      |
| <kbd>super + n</kbd>             | Minimize                                             |
| <kbd>ctrl + shift + n</kbd>      | Restore minimized                                    |
| <kbd>alt + tab</kbd>             | Window switcher                                      |

<br>

**Mouse on the desktop**

| Mousebind        | Action                    |
| ---------------- | ------------------------- |
| `left click`     | Dismiss all notifications |
| `right click`    | App drawer                |
| `middle click`   | Toggle Dashboard          |
| `scroll up/down` | Cycle through tags        |

_... And many many more! for more information, you can check awesome/configuration/keys.lua_

</details>

<h2></h2><br>

**Acknowledgements**

- **Credits**
  - [rxyhn](https://github.com/rxyhn)
  - [ner0z](https://github.com/ner0z)
  - [ChocolateBread799](https://github.com/ChocolateBread799)
  - [JavaCafe01](https://github.com/JavaCafe01)
