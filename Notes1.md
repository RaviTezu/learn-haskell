### For installing Haskell on Ubuntu machine: 
- Haskell platform is already added to the standard PPAs and so you just need to run "sudo apt-get install haskell-platform" to install Haskell on your machine. 

### Some random notes: 
- You can use ghci to open the haskell interpreter.
- Some examples:  
```
ravitezu@Terminator:~$ ghci
GHCi, version 7.6.3: http://www.haskell.org/ghc/  :? for help
Loading package ghc-prim ... linking ... done.
Loading package integer-gmp ... linking ... done.
Loading package base ... linking ... done.
Prelude> 2+1
3
Prelude> take 3 [1,2,3]
[1,2,3]
Prelude> take 3 [1,2,3,4,5,6]
[1,2,3]
Prelude> drop 3 [1,2,3,4,5,6]
[4,5,6]
Prelude> [1,2,3,4,5,6] !! 3
4
Prelude> sum [1,2,3,4,5,6] 
21
Prelude> product [1,2,3,4,5,6] 
720
Prelude> reverse [1,2,3,4,5,6] 
[6,5,4,3,2,1]
```

### Functions in haskell are represented as: 
| Mathematical Functions | Haskell Representation |
|------------------------|------------------------|
| f(x)                   | f x                    |
| f(x,y)                 | f x y                  |
| f(g(x))                | f (g x)                |
| f(x,g(y))              | f x g(y)               |
| f(x)g(y)               | f x * g(y)             |

## Comments in Haskell:
- Comments in Haskell start with "--"
  Ex: -- This is a comment in Haskell

### Infix operator:
- average ns = sum ns `div` length ns
- div is encloded in back quotes.
- x `f` y is just syntactic sugar for f x y

### Some random notes:
- Any function and argumen names must begin with a lower-case letter. 
- By convention, list arguments usually have an s suffix on their name.
  Ex: xs, ns, nss
- In a sequence of definitions, each definition must begin in precisely the same column(white space to be maintained, like Python).
  Ex-1: a = 1
        b = 2 
        c = 3 -- (right)
  Ex-2: a = 1
          b = 2
        c = 3 -- (wrong)
- The layout rules avoid the need for explicit syntax to indicate the grouping of definitions.
  Ex-1: a = b + c
          where
              b = 1
              c = 2
      d = a * 2 --(Implicit grouping, with white space)
  Ex-2: a = b + c
          where
              { b = 1;
                c = 2}
      d = a * 2 --(explicit grouping)
  
## Useful GHCi Commands:
| Command                | Meaning                |
|------------------------|------------------------|
| :load fname            | load script fname      |
| :reload                | reload current script  |
| :edit fname            | edit script fname      |
| :edit                  | edit current script    |
| :type expr             | show type of expr      |
| :?                     | show all commands      |
| :quit                  | quit GHCi              |

### Some random notes:
Putting a function name between single back quotes turns it into a infix operator. GHCi does not automatically detect changes in scripts, one must execute the reload command before using newly added definitions. Types begin with uppercase letters; function and argument names begin with lowercase letters. Whitespaces are significant in Haskell (layout rule).

### For installing hugs on Ubuntu:
- sudo apt-get install hugs
- Hugs, also Hugs 98, is a bytecode interpreter for the functional programming language Haskell.

