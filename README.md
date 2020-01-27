# Shell Clipboard Aliases

## What is it?

Shell aliases to make clipboard use easier.

## Why?

Working with the X Windows clipboard from the terminal is a bit of a pain. You either have to select text to copy and middle click to paste, or select text and use a keyboard shortcut (which is never the usual Ctrl-C for copy, because that's the key combo to kill whatever you're doing).

## yy, pp, gcpp

I created some shell aliases to fix this:

* `yy` copies something to the clipboard
* `pp` pastes the clipboard contents
* `gcpp` executes `git clone <clipboard contents>`

The key combinations are based on copy ('yank') and paste commands from the vi(m) editor

## Examples

### Copy file contents

```
$ yy file.txt
```

Copies the contents of file.txt to the clipboard

### Copy a string

```
$ echo "hello world!"
```

Copies the string "hello world" to the clipboard

### Copy command output

```
ls | yy
```

Copies the output of `ls` to the clipboard

### Paste a string

```
$ pp
```

Outputs the string to the console

### Execute a pasted string

```
``
`pp`
``
```

Executes the pasted string (be super careful when using this)

### Paste into new file

```
pp > file.txt
```

Creates file.txt with contents of the clipboard

### Paste at end of existing file

```
pp >> file.txt
```

Appends clipboard contents to file.txt

### Clone copied git repository

```
gcpp
```

Clones a git repository that has its URL stored in the clipboard

## Usage

Copy the contents of [aliases](aliases) to .bashrc or the relevant file for whichever shell you use
