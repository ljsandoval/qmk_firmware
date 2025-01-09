![SofleKeyboard default keymap](https://i.imgur.com/MZxVvm9.png)
![SofleKeyboard adjust layer](https://i.imgur.com/f5sKy0I.png)

# Default keymap for Sofle Keyboard

Layout in [Keyboard Layout Editor](http://www.keyboard-layout-editor.com/#/gists/76efb423a46cbbea75465cb468eef7ff) and [adjust layer](http://www.keyboard-layout-editor.com/#/gists/4bcf66f922cfd54da20ba04905d56bd4)

Features:

- Symmetric modifiers (CMD/Super, Alt/Opt, Ctrl, Shift)
- Various modes, can be switched (using Adjust layer and the selected one is stored in EEPROM.
- Modes for Qwerty and Colemak support
- Modes for Mac vs Linux/Win support -> different order of modifiers and different action shortcuts on the "UPPER" layer (the red one in the image). Designed to simplify transtions when switching between operating systems often.
- The OLED on master half shows selected mode and caps lock state and is rotated.
- Left encoder controls volume up/down/mute. Right encoder PGUP/PGDOWN. 

Note for my board, i need to build for a different controller by including the `-e CONVERT_TO=promicro_rp2040` flag in flash and build commands, eg:
`qmk flash -kb sofle -km ljsandv1 -e CONVERT_TO=promicro_rp2040`


## My Notes
- Want to test homerow mods
- Switch from mac to pc layout with the same keyboard shortcut used to switch kvm?             
    - My top short cuts that need to switch between mac and pc 
        - Snap windows to left/right/top/bottom/full 
            -  win: gui + arrows
            - mac: ctrl + alt + hjkl
               note: this is changeable to some degree, swiching to cmd + arrows could work would just over ride moving insertion point around but i don't use that much and could rely on vim keys
        - switch desktops 
            - win: gui + ctrl + arrows
            - mac: ctrl + arrows  
        - show desktops
            - win: gui + taba
            - mac: ctrl up?
        - switch windows(alt tab) 
        - copy/paste/cut/undo/selectall
            - win: ctrl + c/v/x/a
            - mac: cmd + c/v/x/a,
        - spotlight (no pc equiv?)
        - close open window
            - pc: alt + F4
            - mac: cmd + q or cmd + w
            
    std win layout left of space: ctrl / win (gui) / alt
    std mac layout left of space: ctrl / alt / cmd (gui)
- would it be too annoying to have space or enter or both use tap dance to double as a layer?
    - left space would activate a layer with arrows on right side
    - left space would activate symbol layer 
    
- Would like to have a gaming layer that moves wasd to be in the positions of esdf to make it feel more right for gaming but that could make typing weird if i have to switch.. j
