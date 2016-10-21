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
tgztree [-v] sourcedirectory [destinationdirectory]
        -v lists directories while packing
        destinationdirectory defaults to sourcedirectory-packed
```

License
-------

See LICENSE.txt
