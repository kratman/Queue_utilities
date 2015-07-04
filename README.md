# Introduction

This repository contains a set of queue utility scripts for the scientific
research groups.

# Brief script documentation 

### Qtop

A queue utility similar to pbstop. It will repeatedly refresh a list of
submitted jobs on a queue or for a user. It will also replace usernames with
real names. A usernames file should be referenced by the a ${QtopUserNames}
environment variable.

```
user:$ Qtop -q [ queue name ]
user:$ Qtop -r [ user name ]
user:$ Qtop -u [ user name ]
user:$ Qtop -u me
user:$ Qtop --help

 -q => show jobs on a queue
 -r => show running jobs for a user
 -u => show all jobs for a user, 'me' is shorthand for the current user
 --help, -h => print full help

Press "q" and "enter" to exit Qtop.
```

### MyQueue

A script to print a list of running and queued jobs for the current
user. The output is essentially the same as Qtop.

```
user:$ MyQueue
```

### SCPpath

A script to print the username, server, and path for scp or rsync.
The currently the server name must be set in the script.

```
user:$ SCPpath [ optional, path/file ]
```

