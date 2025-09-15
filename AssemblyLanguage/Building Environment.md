> System : Ubuntu 24.04.3

First, install the open-source MS-DOS emulator **DOSBOX**:
`$ sudo apt-get install dosbox`

Launch it once to generate the config folder:
 `$ dosbox` 

and then
```bash
$ cd ~/.dosbox/
$ vim dosbox-0.74-3.conf #depends on your dosbox version
# now add "mount c /path/to/yourfolder" & "c:" to the end of the file 

```

once you are set, start dosbox `$ dosbox` again, and you will see your chosen folder has been mounted as drive C:.

