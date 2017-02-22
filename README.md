tgztree - script to create "tgz"s by directory in a tree

This script makes a copy of a directory tree with one change,
create a gzipped tar in each directory instead of original files.

This can be usefull if you want to store your files into IDA
and keep the original directory structure but transferring a
lot of separate small files is too slow. First create the new data
directory with this script and then transfer the new directory
into IDA with for instance iput_wrapper script.

Usage
-----

```
tgztree [-v] [-b size [-d]] sourcedirectory [destinationdirectory]
       The order of paramaters must be as listed
       -v list directories while packing
       -b split result files to the size
        Linux (GNU split) K, M, G for 1024 based and KB, MB, GB for 1000 based
          Example: "tgztree -b 500M mydirectory"
        OSX (old BSD split) k, m for 1024 based kilo and mega
          Example: "tgztree -b 500m mydirectory"
       -d split output uses -d option, sequential numbers
       destinationdirectory defaults to sourcedirectory-packed
```

License
-------

See LICENSE.txt
