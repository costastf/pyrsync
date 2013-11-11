pyrsync
=======

(pronounced piercing). Python lightweight rsync wrapper. Useful for using rsync in python projects.

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


