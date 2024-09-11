# Hello!
This is a series of scripts that I use to feel more at home in my shell
So first, install fish!
Then put these commands:
```fish
    # eliminate the annoying greeting
    set -U fish_greeting ""
    fish_vi_key_bindings
```
```fish
# install fisher
curl -sL https://raw.githubusercontent.com/jorgebucaran/fisher/main/functions/fisher.fish | source && fisher install jorgebucaran/fisher
```
Now let's get to install a couple of plugins that you may end up using anyway
```fish
    fisher install jorgebucaran/nvm.fish
    fisher install IlanCosman/tide@v6
    fisher install jethrokuan/z
    fisher install joehillen/to-fish
```
Finally, this one is extremely personal, but I want to use icons and certain way of doing things in tide, this basic config should work:
```fish
tide configure --auto --style=Rainbow --prompt_colors='True color' --show_time=No --rainbow_prompt_separators=Round --powerline_prompt_heads=Round --powerline_prompt_tails=Round --powerline_prompt_style='Two lines, character and frame' --prompt_connection=Dotted --powerline_right_prompt_frame=No --prompt_connection_andor_frame_color=Lightest --prompt_spacing=Sparse --icons='Many icons' --transient=Yes
```
Now, put the indicator of the vim mode at the far left, set all of the background colors to rosé, and change the icons:
```fish
    set --universal tide_left_prompt_items vi_mode $tide_left_prompt_items
    set tide_vi_mode_bg_color_default eb6f92
    set tide_vi_mode_bg_color_insert eb6f92
    set tide_vi_mode_bg_color_visual eb6f92
    set tide_vi_mode_bg_color_replace eb6f92
    set tide_vi_mode_icon_default 
    set tide_vi_mode_icon_insert 
    set tide_vi_mode_icon_visual 󰼢
    set tide_vi_mode_icon_replace 
```

I also like to use lambda (for the lambda calculus) as a prompt
```fish
    set tide_character_icon 󰘧
    set tide_character_vi_icon_default 󰘧
    set tide_character_vi_icon_visual 󰘧
    set tide_character_vi_icon_replace 󰘧
    set tide_character_color 908caa
```
