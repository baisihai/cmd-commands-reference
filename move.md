## MOVE Command
Moves files and renames files and directories.

## Syntax
```batchfile
To move one or more files:
MOVE [/Y | /-Y] [drive:][path]filename1[,...] destination

To rename a directory:
MOVE [/Y | /-Y] [drive:][path]dirname1 dirname2

  [drive:][path]filename1   Specifies the location and name of the file
                            or files you want to move.
  destination               Specifies the new location of the file. Destination
                            can consist of a drive letter and colon, a
                            directory name, or a combination. If you are moving
                            only one file, you can also include a filename if
                            you want to rename the file when you move it.
  [drive:][path]dirname1    Specifies the directory you want to rename.
  dirname2                  Specifies the new name of the directory.

  /Y                        Suppresses prompting to confirm you want to
                            overwrite an existing destination file.
  /-Y                       Causes prompting to confirm you want to overwrite
                            an existing destination file.

The switch /Y may be present in the COPYCMD environment variable.
This may be overridden with /-Y on the command line.  Default is
to prompt on overwrites unless MOVE command is being executed from
within a batch script.
```

## Examples
**1. Move all files from source directory to destination directory.**
```batchfile
move c:\windows\temp\*.* c:\temp
```

**2. Move a directory or file with name that contains space(s).**  
If your directory name or file name contains space(s), it must be surrounded with quotes, otherwise you get a "The syntax of the command is incorrect." error message.
```batchfile
move "computer hope" example
```
