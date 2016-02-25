# regcache
A holder for regular expressions. This will print out a regular expression to stdout.
This should keep the user from having to type out long complicated regular expressions.
# Usage
```
$ ip addr | grep -P `regcache mac`
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    link/ether fa:ee:67:89:09:43 brd ff:ff:ff:ff:ff:ff
    link/ether d4:b2:11:89:75:e4 brd ff:ff:ff:ff:ff:ff
```

# Install
Copy the regcache file to anywhere that's inside your PATH variable and edit the value of FULL_CONF
to the regex cache you want to have loaded. FULL_CONF has to be a text file that is a valid JSON string.

# HELP!!!
```
usage: regcache [-h] [-d] [-t] [-c CACHE] [-j] [-a] [--rem] [--init] [REGEX]

positional arguments:
  REGEX                 The regex to operate on.

optional arguments:
  -h, --help            show this help message and exit
  -d, --detail          This will print all information known about a regular
                        expression.
  -t, --title           Print regular expressions with titles only.
  -c CACHE, --cache CACHE
                        Force differnet regular expression cache.
  -j, --json            Print out the json cached file.
  -a, --add             Add a new regex to the cache.
  --rem                 This will remove the provided regex from the cache.
  --init                This will initalize a new cache on the path of
                        FULL_CONF.
```
