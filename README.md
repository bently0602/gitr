gitr
====

Shell script wrapper around git.

Uses [Dropbox-Uploader](https://github.com/andreafabrizi/Dropbox-Uploader)

--identity-file Derivied From:
Wrapper script that can specify an ssh-key file with the Git command
The MIT License (MIT) - http://opensource.org/licenses/MIT
Copyright (c) 2013 Alvin Abad

I install with 
```
ln -s gitr /usr/bin/gitr
ln -s dropbox_uploader /usr/bin/dropbox_uploader
```


```
usage: gitr
    [-i|--identity-file]
    [-rb|--remote-backup|xbackup]
    [-rr|--remote-restore|xrestore]
    [-xc|-xcom|xcommit]
    [xadd]
    [xgenkey|-xk]
options:
    - use a specified identity key
    gitr -i ssh-key-file normal-git-commands
    
    - restore repo to a backuped dropbox one (made with rb)
    gitr -rr /Path/To/dropbox_uploader/settings_file repo-test

    - backup repo to dropbox as gzip2, encrypted by openssl with a given name
    gitr -rb /Path/To/dropbox_uploader/settings_file repo-test
    
    - shortcut for git commit -m "MSG"
    gitr xcom "Commit Message"

    - shortcut for git add -A .
    gitr xadd

    - generate key for git
    gitr xgenkey

    - if gitr has commands that are not gitr commands
    - it forward them to git.
    gitr checkout master
    - is the same as
    git checkout master
```    
