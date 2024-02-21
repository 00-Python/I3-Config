# i3 Window Manager Configuration File Boilerplate

This repository contains the configuration file (`config`) for the i3 window manager, tailored for the Manjaro Linux distribution. Below is an explanation of the keybindings and their corresponding code snippets in the configuration file.

## Keybindings

### General Keybindings

- **Mod+Return**: Open terminal (Alacritty)
  ```bash
  bindsym $mod+Return exec alacritty
  ```

- **Mod+Shift+q**: Kill focused window
  ```bash
  bindsym $mod+Shift+q kill
  ```

- **Mod+Shift+r**: Restart i3
  ```bash
  bindsym $mod+Shift+r restart
  ```

- **Mod+Shift+e**: Exit i3
  ```bash
  bindsym $mod+Shift+e exec "i3-nagbar -t warning -m 'Do you really want to exit i3?' -b 'Yes, exit i3' 'i3-msg exit'"
  ```

- **Mod+Shift+c**: Reload configuration file
  ```bash
  bindsym $mod+Shift+c reload
  ```

- **Mod+1, Mod+2, Mod+3, Mod+4**: Switch to workspaces 1, 2, 3, 4
  ```bash
  bindsym $mod+1 workspace number 1
  bindsym $mod+2 workspace number 2
  bindsym $mod+3 workspace number 3
  bindsym $mod+4 workspace number 4
  ```

- **Mod+Right, Mod+Left**: Move to next/previous workspace
  ```bash
  bindsym $mod+Right workspace next
  bindsym $mod+Left workspace prev
  ```

### Application Launch Keybindings

- **Mod+Shift+f**: Launch Firefox
  ```bash
  bindsym $mod+Shift+f exec firefox
  ```

- **Mod+Shift+v**: Launch VSCode
  ```bash
  bindsym $mod+Shift+v exec code
  ```

- **Mod+Shift+m**: Launch Thunar (File Manager)
  ```bash
  bindsym $mod+Shift+m exec thunar
  ```

### Navigation Keybindings

- **Mod+j**: Focus left
  ```bash
  bindsym $mod+j focus left
  ```

- **Mod+k**: Focus down
  ```bash
  bindsym $mod+k focus down
  ```

- **Mod+l**: Focus up
  ```bash
  bindsym $mod+l focus up
  ```

- **Mod+;**: Focus right
  ```bash
  bindsym $mod+semicolon focus right
  ```

### Window Movement Keybindings

- **Mod+Shift+j**: Move window left
  ```bash
  bindsym $mod+Shift+j move left
  ```

- **Mod+Shift+k**: Move window down
  ```bash
  bindsym $mod+Shift+k move down
  ```

- **Mod+Shift+l**: Move window up
  ```bash
  bindsym $mod+Shift+l move up
  ```

- **Mod+Shift+;**: Move window right
  ```bash
  bindsym $mod+Shift+semicolon move right
  ```

### Layout Keybindings

- **Mod+b**: Switch to stacking layout
  ```bash
  bindsym $mod+b layout stacking
  ```

- **Mod+s**: Switch to stacking layout
  ```bash
  bindsym $mod+s layout stacking
  ```

- **Mod+w**: Switch to tabbed layout
  ```bash
  bindsym $mod+w layout tabbed
  ```

- **Mod+e**: Toggle split layout
  ```bash
  bindsym $mod+e layout toggle split
  ```

### Miscellaneous Keybindings

- **Mod+f**: Toggle fullscreen for the focused window
  ```bash
  bindsym $mod+f fullscreen toggle
  ```

- **Mod+a**: Focus the parent container
  ```bash
  bindsym $mod+a focus parent
  ```

### Window Resizing Keybindings (While in Resize Mode)

- **h**: Shrink window width
- **j**: Grow window height
- **k**: Shrink window height
- **l**: Grow window width
- **Enter**: Exit resize mode
- **Escape**: Exit resize mode

## Editing and Customizing the Configuration

To edit and customize the i3 configuration file:

1. Clone this repository to your local machine using Git:
   ```bash
   git clone <repository_url>
   ```

2. Navigate to the cloned repository directory:
   ```bash
   cd <repository_name>
   ```

3. Open the `config` file in a text editor of your choice. You can customize keybindings, colors, fonts, and other settings according to your preferences.

4. Save the changes after customization.

## Copying the Configuration to the Correct Location

Once you've made your customizations, follow these steps to copy the configuration to the correct location:

1. Navigate to the i3 configuration directory:
   ```bash
   cd ~/.config/i3/
   ```

2. Make a backup of your existing configuration file (optional but recommended):
   ```bash
   cp config config_backup
   ```

3. Copy the modified `config` file from the cloned repository to the i3 configuration directory:
   ```bash
   cp <path_to_cloned_repository>/config .
   ```

4. Restart i3 for the changes to take effect:
   ```bash
   i3-msg restart
   ```

Now, your customized i3 configuration should be applied.
