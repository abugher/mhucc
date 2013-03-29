mhucc checks whether a user exists on a list of remote systems.  The
existence of a user is currently determined by checking for his name
/etc/passwd and several other text files.  It doesn't do anything you
couldn't do reasonably quickly with ssh and grep.

The default output is a listing of files that match.  "-v" will add the
matching lines from those files to the output.  "-b" will switch to
Boolean per-host output -- essentially just "match" or "no match".

The behavior is likely to change quite a bit, and some further polishing
is called for.  I've found it to be useful as-is, though.
