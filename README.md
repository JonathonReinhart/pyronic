pyronic
=======
Run a program and silence its output, unless it fails.

pyronic is a replacement for [chronic](https://joeyh.name/code/moreutils/).

One key difference is that pyronic, in its default mode, will preserve the
relative order of the lines written by program to stdout and stderr. Some
programs aren't consistent in printing to stdout or stderr, and this order can
make errors much eaiser to comprehend.

```
$ chronic ./test/interleave
1 stdout
2 stdout
4 stdout
7 stdout
9 stdout
3 stderr
5 stderr
6 stderr
8 stderr

$ pyronic ./test/interleave
1 stdout
2 stdout
3 stderr
4 stdout
5 stderr
6 stderr
7 stdout
8 stderr
9 stdout
```
