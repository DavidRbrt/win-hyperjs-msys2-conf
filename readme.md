# MSYS2 Hyper configuration

update MSYS2 **.bashrc** (/home/<_user_>/.bashrc):

```
# Perso
## Home
export MSYS_HOME=$HOME
export HOME=/c/Users/<user>
cd $HOME

## Prompt
git_branch() {
     git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/(\1)/'
}
export PS1="\[\e[33m\]\w \[\033[35m\]\$(git_branch) \[\033[96m\]> \[\033[0m\]"

```

update **.hyper.js** (~\AppData\Roaming\Hyper\.hyper.js):

```
shell: 'C:\\msys64\\msys2_shell.cmd',
shellArgs: [
    '-mingw64',
    '-defterm',
    '-no-start',
    '-full-path'
],
```

udpdate vscode **.settings.json** (~\AppData\Roaming\Code\User\settings.json):

```
"terminal.integrated.profiles.windows": {
    "msys": {
    "path": "C:\\msys64\\msys2_shell.cmd",
    "args": ["-mingw64", "-defterm", "-no-start", "-full-path", "-file"]
    }
},
"terminal.integrated.defaultProfile.windows": "msys",
```