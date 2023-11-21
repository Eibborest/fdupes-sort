# fdupes-sort

This is a one liner my friend Michael Anthon (MrChook)  made back in 2006 for sorting the output of fdupes by file size.

It's been handy over the years so I though I would share it here.  

cat fdupesoutput.txt |  perl -00 -le 'print map $_->[1], sort{$a->[0]<=>$b->[0]} map [/(\d+) bytes/, $_], <>'
