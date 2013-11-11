pyrsync
=======

(pronounced piercing). Python lightweight rsync wrapper. 
Useful for using rsync in python projects.

This library wraps rsync in an object oriented manner. Upon instantiation it searches for the rsync executable. It uses "which" in linux and looks at the local folder in windows. It can work with a cygwin statically compiled rsync. In windows it automatically changes the paths in cygwin compatible paths. (It has not been thoroughly tested in windows.) It's usage is as follows.

Usage :
``` 
    backup = Sync()
    backup.source           = r'c:\Documents And Settings\user\Desktop'
    backup.destination      = r'x:\backup' 

    # backup.options.defaults() sets the following settings to True 
    # humanReadable, verbose, links, recursive, permissions, executability, 
    # owner, group, times, delete, ignoreErrors, force, stats

    # exclude options should be space delimited
    backup.options.exclude  = '*.mp3 *.jpg'
    
    # Individual settings can be set
    backup.options.links    = False
    backup.run()
    
```


