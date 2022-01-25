# MSYS2 Hyper configuration

update hyper.js (~\AppData\Roaming\Hyper) file with this:

```
shell: 'C:\\msys64\\msys2_shell.cmd',
shellArgs: [
    '-mingw64',
    '-defterm',
    '-no-start',
    '-full-path',
    '-where',
    'C:\\Users\\David'
],
```