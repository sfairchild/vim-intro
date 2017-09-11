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

## 0 ^ and $

| `0` | Go to the very beginning of the line           |
| `^` | Go to the first none blank character of a line |
| `$` | Go to the end of a line                        |

## Navigate by word and WORD

By word

`b` `ge` `w` `e`

By WORD

`B` `gE` `W` `E`

#### word

A word consists of a sequence of letters, digits and underscores, or a
sequence of other non-blank characters, separated with white space (spaces,
tabs, <EOL>).  This can be changed with the 'iskeyword' option.  An empty line
is also considered to be a word.

#### WORD

A WORD consists of a sequence of non-blank characters, separated with white
space.  An empty line is also considered to be a WORD.

## Find characters with (f)ind and (t)ill

`F{char}` `T{char}` `f{char}` `t{char}`

Repeat your find in the same direction with `;` and reverse with `,`

## Navigate to a line number or beginning/end of file

| `gg`                        | BOF               |
| `{number}gg` or `{number}G` | Go to line Number |
| `G`                         | EOF               |

## Search for text

 | `/{text}` | search forwards for 'text'                        |
 | `?{text}` | search backwards for 'text'                       |
 | `*`       | search forward for the closest word to the cursor |
 | `n`       | continue last search in the same direction        |
 | `N`       | continue last search in the opposite direction    |


```
 _____                    _    ___  ___          _      
|_   _|                  | |   |  \/  |         | |     
  | | _ __  ___  ___ _ __| |_  | .  . | ___   __| | ___ 
  | || '_ \/ __|/ _ \ '__| __| | |\/| |/ _ \ / _` |/ _ \
 _| || | | \__ \  __/ |  | |_  | |  | | (_) | (_| |  __/
 \___/_| |_|___/\___|_|   \__| \_|  |_/\___/ \__,_|\___|
```                                                        

## ESC(escape)

Use `ESC` to exit insert mode

## Insert and Append

`I` `i` `a` `A`

## o and O

`o` make new line below current position and enter insert
`O` make new line above current position and enter insert


```
 _____                      _   _                 
|  _  |                    | | (_)                
| | | |_ __   ___ _ __ __ _| |_ _  ___  _ __  ___ 
| | | | '_ \ / _ \ '__/ _` | __| |/ _ \| '_ \/ __|
\ \_/ / |_) |  __/ | | (_| | |_| | (_) | | | \__ \
 \___/| .__/ \___|_|  \__,_|\__|_|\___/|_| |_|___/
      | |                                         
      |_|                                         
```

## Anatomy of a motion

(count)[operation]{motion}

## Common operations

| key    | description      |
| ------ | ---------------- |
| `d`    | delete text      |
| `c`    | change text      |
| `y`    | yank text        |
| `=`    | auto indent      |
| `<`    | shift left       |
| `>`    | shift right      |
| `g~`   | swap case        |
| `gu`   | make lowercase   |
| `gU`   | make UPPERCASE   |


```
______           _     _                
| ___ \         (_)   | |               
| |_/ /___  __ _ _ ___| |_ ___ _ __ ___ 
|    // _ \/ _` | / __| __/ _ \ '__/ __|
| |\ \  __/ (_| | \__ \ ||  __/ |  \__ \
\_| \_\___|\__, |_|___/\__\___|_|  |___/
            __/ |                       
           |___/                       
```

## Copy & Paste

| vim command     | vim verb   | equivalent command  |
| -------------   | ---------- | ------------------- |
| `y`             | yank       | copy                |
| `p`             | put        | paste               |
| `d` `x` `s` `c` | delete     | cut                 |

## Most used registers

| `"a-"z` | user assigned register    |
| ---     | ---                       |
| `"`     | 'unnamed' register        |
| `"+`    | system clipboard          |
| `"0`    | yank register             |
| `"1-"9  | Last delete/yank register |

## Other helpful registers

| `"%` | Current file name   |
| ---  | ---                 |
| `".` | Last inserted text  |
| `":` | Last Ex command     |
| `"/` | Last search pattern |

## Using named registers

Lowercase letters overwrite the named register.

Uppercase letters append to the named register.

`"ayw` writes the current word to the `a` register 

`"Ayw` appends the current word to the `a` register 
