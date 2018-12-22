JC-Style-Terminal-Theme
==================
### Description

This is my mac terminal profile and configuration for default macos terminal.app .

### To Generate Preview ScreenShots
* In the terminal, Run `bash tools/preview.sh`

Reference: [Bash Prompt HOWTO: Chapter 6. ANSI Escape Sequences: Colours and Cursor Movement][ref]

[ref]: http://tldp.org/HOWTO/Bash-Prompt-HOWTO/x329.html

### Installation Instructions
* Install Ubuntu font [here][1]
* `*.terminal` file -> Open Terminal/ Preference/ Add
* Edit Font: Ubuntu Mono 13p
* In the `~/.bash_profile` -> Copy & Paste the text below

[1]: https://design.ubuntu.com/font/

---


### Terminal Theme Configuration ###

#### Make ls use colors
```
# Make ls use colors
export CLICOLOR=1
alias ls='ls -Fa'
```
#### Define colors
```
# Define colors
C_DEFAULT="\[\033[m\]"
C_WHITE="\[\033[1m\]"
C_BLACK="\[\033[30m\]"
C_RED="\[\033[31m\]"
C_GREEN="\[\033[32m\]"
C_YELLOW="\[\033[33m\]"
C_BLUE="\[\033[34m\]"
C_PURPLE="\[\033[35m\]"
C_CYAN="\[\033[36m\]"
C_LIGHTGRAY="\[\033[37m\]"
C_DARKGRAY="\[\033[1;30m\]"
C_LIGHTRED="\[\033[1;31m\]"
C_LIGHTGREEN="\[\033[1;32m\]"
C_LIGHTYELLOW="\[\033[1;33m\]"
C_LIGHTBLUE="\[\033[1;34m\]"
C_LIGHTPURPLE="\[\033[1;35m\]"
C_LIGHTCYAN="\[\033[1;36m\]"
C_BG_BLACK="\[\033[40m\]"
C_BG_RED="\[\033[41m\]"
C_BG_GREEN="\[\033[42m\]"
C_BG_YELLOW="\[\033[43m\]"
C_BG_BLUE="\[\033[44m\]"
C_BG_PURPLE="\[\033[45m\]"
C_BG_CYAN="\[\033[46m\]"
C_BG_LIGHTGRAY="\[\033[47m\]"
```
#### Display git branch name
```
# Display git branch name
parse_git_branch() {
    git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}
```
#### Set the prompt
```
# Set the prompt
export PS1="\n$C_LIGHTGREEN\u$C_DARKGRAY@$C_BLUE\h$C_DARKGRAY: $C_LIGHTYELLOW\w $C_LIGHT_GREEN\$(parse_git_branch)\n$C_DARKGRAY\$$C_DEFAULT " 
```

Screenshots
==================
![JC-Style][img1][img2]

[img1]: https://github.com/jcwu1717/JC-Style-Terminal-Theme/blob/master/Screenshots/JC%20Style.png
[img2]: https://github.com/jcwu1717/JC-Style-Terminal-Theme/blob/master/Screenshots/Terminal%20Screenshot.png
