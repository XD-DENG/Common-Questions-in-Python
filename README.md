# Common-Questions-in--Python
A collection of common questions about Python I encountered, and corresponding solutions

## 1. How to get the current time in Python?
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

## 2. How to get current directory and change the directory?

```
>>> import os
>>> os.getcwd()
'/Users/nus/Documents'
>>> os.chdir("/Users/nus")
>>> os.getcwd()
'/Users/nus'
```
