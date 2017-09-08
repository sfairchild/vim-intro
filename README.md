# Introduction to VIM

An introduction to one of the most powerful and widely available text editors.



```
______              _        ___  ___        _    _                    
| ___ \            (_)       |  \/  |       | |  (_)                   
| |_/ /  __ _  ___  _   ___  | .  . |  ___  | |_  _   ___   _ __   ___ 
| ___ \ / _` |/ __|| | / __| | |\/| | / _ \ | __|| | / _ \ | '_ \ / __|
| |_/ /| (_| |\__ \| || (__  | |  | || (_) || |_ | || (_) || | | |\__ \
\____/  \__,_||___/|_| \___| \_|  |_/ \___/  \__||_| \___/ |_| |_||___/
```                                                                       

## hjkl


```
       k                up
                                                                                 
   h        l     left      right
                                                           
       j               down
```

## Navigate by word and WORD

By word

```b``` ```ge``` ```w``` ```e```

By WORD

```B``` ```gE``` ```W``` ```E```

#### word

A word consists of a sequence of letters, digits and underscores, or a
sequence of other non-blank characters, separated with white space (spaces,
tabs, <EOL>).  This can be changed with the 'iskeyword' option.  An empty line
is also considered to be a word.

#### WORD

A WORD consists of a sequence of non-blank characters, separated with white
space.  An empty line is also considered to be a WORD.

## Find charecters with (f)ind and (t)ill

```F{char}``` ```T{char}``` ```f{char}``` ```t{char}```

Repeat your find in the same direction with ```;``` and reverse with ```,```

## Navigate to a line number or beginning/end of file

* ```gg``` BOF
* ```{number}gg``` or ```{number}G``` Line Number
* ```G``` EOF
