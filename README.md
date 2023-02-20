# ncpro

This is a quick commandline viewer for the ncdb files created by NoteCase Pro.

It looks like this:

```
$ ncpro help
usage: ncpro [-d database] CMD [PARAMS...]
CMD can be one of:
        list      - list child notes
        print     - print note contents
        show      - alias for print
        edit      - open editor and change note
        find      - find notes with matching string
        markdown  - set all notes without syntax to markdown
```

You can list your notes:

```
$ ncpro list
 • /Linux - 33
 • /Windows - 19
```

And you can drill down into deeper levels:

```
$ ncpro list /Linux
    • /Linux/apt
    • /Linux/awk
    ...
```

Then print the article you want:

```
$ ncpro print /Linux/awk
/Linux/awk

   Print lines between a pattern

    awk '/start/,/end/'

   Sort lines by length

    awk '{ print length, $0 }' | sort -g

...
```

You can even edit a note with `$EDITOR`:

```
$ ncpro edit /Linux/awk
```

Will open it in vim.
