
[//]: # (Mixture of GitHub markdown and HTML. HTML is needed for formatting.)

<div align=center> <h2>
Queue Utilities Documentation
</h2> </div>

### Introduction

This repository contains a set of queue utility scripts for the scientific
research groups. These scripts are not intended to replace Linux utilities,
but rather to provide simplified utilities for minimalist clusters.

### Brief overview of the scripts

#### Qtop

A queue utility similar to pbstop. It will repeatedly refresh a list of
submitted jobs on a queue or for a user. It will also replace usernames with
real names. A usernames file should be referenced by the a ${QtopUserNames}
environment variable. An example QtopUserNames file is included with the
repository. Color settings can be changed in the python script.

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

Pressing enter refreshes the output and pressing 'q' then enter exits Qtop.
```

NB: Python 2.7 or higher is required due to a change in the subprocess module.

#### MyQueue

A script to print a list of running and queued jobs for the current
user. The output is similar to 'Qtop -u me' without automatically refreshing.

```
user:$ MyQueue
```

NB: Python 2.7 or higher is required due to a change in the subprocess module.

#### SCPpath

A script to print the username, server, and path for scp or rsync.
The currently the server name must be set in the script.

```
user:$ SCPpath [ optional, /path/to/file ]
```

#### CatSCP

A script to run cat on a remote file.

```
user:$ CatSCP user@server:/path/to/file
```
