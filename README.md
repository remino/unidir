unidir
======

```
unidir 1.0.3

Usage: unidir [options] src1 [src2 srcn...] dst

Unify the content of multiple directories into one using symlinks.

The first directory will have priority if symlinks are not overridden when present.

Available options:

	-f        Override symlinks if one is present.
	-h        This help screen.

Example:

	src/
		1/a
		2/a
		3/b
	dst/

	% unidir src/* dst

	# If -f is not set:

	dst/
		1/a -> ../src/1/a
		3/b -> ../src/3/b

	# If -f is set:

	dst/
		2/a -> ../src/2/a
		3/b -> ../src/3/b

```

