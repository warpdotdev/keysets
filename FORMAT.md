# Keybindings File Format

The keybindings file is a [yaml](https://yaml.org/) file with a top-level map of action names to key
bindings. Both the action name and the key binding are string values.

_Compatibility Note_: Warp is still in Beta and this format is subject to change.

## Key Bindings

The format for the key bindings is a hyphen-separated list of modifiers ending with the key. For
example, `cmd-ctrl-g` represents `Command + Control + G`

### Modifiers

The possible modifiers on Mac are:

- `ctrl`: Control
- `cmd`: Command
- `alt`: Option
- `meta`: Meta key
- `shift`: Shift

The possible modifiers on Windows or Linux are:

- `ctrl`: Control
- `ctrl-shift`: Windows, Super, or System
- `alt`: Alt
- `meta`: Meta key
- `shift`: Shift

### Keys

The keys are the character produced by the key, or a description of the key for non-printing keys.
The available non-printing keys are:

- `up`
- `down`
- `left`
- `right`
- `home`
- `end`
- `pageup`
- `pagedown`
- `backspace`
- `enter`
- `insert`
- `delete`
- `escape`
- `tab`
- `numpadenter`
- `f1`
- `f2`
- `f3`
- `f4`
- `f5`
- `f6`
- `f7`
- `f8`
- `f9`
- `f10`
- `f11`
- `f12`
- `f13`
- `f14`
- `f15`
- `f16`
- `f17`
- `f18`
- `f19`
- `f20`

### Notes and Examples

For a printable key, the value must take into account the presence of the `shift` modifier. So to
set a keybinding for `Command + Shift + A`, you would use (note the capitalization):

```markdown
cmd-shift-A
```

While to set a keybindings for `Command + A`, you would use:

```markdown
cmd-a
```

## Action Names

The available actions and their names are listed in the table below:

| Action Description                 | YAML File Name                                              |
| ---------------------------------- | ----------------------------------------------------------- |
| Add cursor below                   | editor_view:add_cursor_below                                |
| Add cursor above                   | editor_view:add_cursor_above                                |
| Fold selected ranges               | editor_view:fold_selected_ranges                            |
| Unfold                             | editor_view:unfold                                          |
| Fold                               | editor_view:fold                                            |
| Add selection for next occurrence  | editor_view:add_next_occurrence                             |
| Copy and clear selected lines      | editor_view:clear_and_copy_lines                            |
| Select to end of line              | editor:select_to_line_end                                   |
| Select to start of line            | editor:select_to_line_start                                 |
| Accept Autosuggestion              | editor_view:insert_autosuggestion_text_and_update_selection |
| Delete all left                    | editor_view:delete_all_left                                 |
| Delete all right                   | editor_view:delete_all_right                                |
| Cut all right                      | editor_view:cut_all_right                                   |
| Clear selected lines               | editor_view:clear_lines                                     |
| Delete word right                  | editor:delete_word_right                                    |
| Cut word right                     | editor_view:cut_word_right                                  |
| Delete word left                   | editor:delete_word_left                                     |
| Cut word left                      | editor_view:cut_word_left                                   |
| Clear command editor               | editor_view:clear_buffer                                    |
| Remove the previous character      | editor_view:backspace                                       |
| Move to the end of the buffer      | editor_view:move_to_buffer_end                              |
| Move to the start of the buffer    | editor_view:move_to_buffer_start                            |
| Move to the end of the paragraph   | editor_view:move_to_paragraph_end                           |
| Move to the start of the paragraph | editor_view:move_to_paragraph_start                         |
| Move backward one word             | editor_view:move_backward_one_word                          |
| Move forward one word              | editor_view:move_forward_one_word                           |
| Move cursor to the bottom          | editor_view:cmd_down                                        |
| End                                | editor_view:end                                             |
| Home                               | editor_view:home                                            |
| Move to end of line                | editor_view:move_to_line_end                                |
| Move to start of line              | editor_view:move_to_line_start                              |
| Select all                         | editor_view:select_all                                      |
| Select down                        | editor_view:select_down                                     |
| Select up                          | editor_view:select_up                                       |
| Select one character to the right  | editor_view:select_right                                    |
| Select one character to the left   | editor_view:select_left                                     |
| Select one word to the right       | editor_view:select_right_by_word                            |
| Select one word to the left        | editor_view:select_left_by_word                             |
| Clear screen                       | input:clear_screen                                          |
| Search command history             | input:search_command_history                                |
| Clear blocks                       | terminal:clear_lines                                        |
| Find                               | terminal:find                                               |
| Re-input selected command as root  | terminal:reinput_command_with_sudo                          |
| Re-input selected command          | terminal:reinput_command                                    |
| Share selected block               | terminal:open_share_modal                                   |
| Copy command                       | terminal:copy_command                                       |
| Copy command output                | terminal:copy_output                                        |
| Select next block                  | terminal:select_next_block                                  |
| Select previous block              | terminal:select_previous_block                              |
| Copy                               | terminal:copy                                               |
| Paste                              | terminal:paste                                              |
| Focus terminal input               | terminal:focus_input                                        |
| Resize pane > Move divider down    | pane_group:resize_down                                      |
| Resize pane > Move divider up      | pane_group:resize_up                                        |
| Resize pane > Move divider right   | pane_group:resize_right                                     |
| Resize pane > Move divider left    | pane_group:resize_left                                      |
| Switch panes down                  | pane_group:navigate_down                                    |
| Switch panes up                    | pane_group:navigate_up                                      |
| Switch panes right                 | pane_group:navigate_right                                   |
| Switch panes left                  | pane_group:navigate_left                                    |
| Split pane down                    | pane_group:add_vertical                                     |
| Split pane right                   | pane_group:add_horizontal                                   |
| Navigate to next pane              | pane_group:navigate_next                                    |
| Navigate to previous pane          | pane_group:navigate_prev                                    |
| Open keybindings editor            | workspace:show_keybinding_settings                          |
| Toggle command palette             | workspace:toggle_command_palette                            |
| Open theme picker                  | workspace:show_theme_chooser                                |
| Reset font size to default         | workspace:reset_font_size                                   |
| Decrease font size                 | workspace:decrease_font_size                                |
| Increase font size                 | workspace:increase_font_size                                |
| Activate next tab                  | workspace:activate_next_tab                                 |
| Activate previous tab              | workspace:activate_prev_tab                                 |
| Open settings                      | workspace:show_settings_modal                               |
