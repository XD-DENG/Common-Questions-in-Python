## Common-Questions-in--Python
A collection of common questions about Python I encountered, and corresponding solutions

### 1. How to get the current time in Python?
```
>>> import datetime
>>> datetime.datetime.now()
datetime.datetime(2015, 10, 9, 17, 15, 30, 498779)
>>> test = datetime.datetime.now()
>>> test.date()
datetime.date(2015, 10, 9)
>>> test.time()
datetime.time(17, 15, 38, 72927)
```

### 2. How to get current directory and change the directory?

```
>>> import os
>>> os.getcwd()
'/Users/nus/Documents'
>>> os.chdir("/Users/nus")
>>> os.getcwd()
'/Users/nus'
```

### 3. How to get the current user name?

```
>>> import pwd
>>> import os
>>> pwd.getpwuid(os.getuid())
pwd.struct_passwd(pw_name='nus', pw_passwd='********', pw_uid=501, pw_gid=20, pw_gecos='NUS', pw_dir='/Users/nus', pw_shell='/bin/bash')
>>> pwd.getpwuid(os.getuid())[5]
'/Users/nus'
>>> pwd.getpwuid(os.getuid())[0]
'nus'
```

```
>>> from getpass import getuser
>>> getuser()
'nus'
```


### 4. How to get the path of the current script?

```
# Please note this only works for script, and does NOT work interactively.
import os
print os.path.realpath(__file__)
```

