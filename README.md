# Go Cheat Sheet

# Index
1. [Basic Syntax](#basic-syntax)
2. [Operators](#operators)
    * [Arithmetic](#arithmetic)
    * [Comparison](#comparison)
    * [Logical](#logical)
    * [Other](#other)
3. [Declarations](#declarations)
4. [Functions](#functions)
    * [Functions as values and closures](#functions-as-values-and-closures)
    * [Variadic Functions](#variadic-functions)
5. [Built-in Types](#built-in-types)
6. [Type Conversions](#type-conversions)
7. [Packages](#packages)
8. [Control structures](#control-structures)
    * [If](#if)
    * [Loops](#loops)
    * [Switch](#switch)
9. [Arrays, Slices, Ranges](#arrays-slices-ranges)
    * [Arrays](#arrays)
    * [Slices](#slices)
    * [Operations on Arrays and Slices](#operations-on-arrays-and-slices)
10. [Maps](#maps)
11. [Structs](#structs)
12. [Pointers](#pointers)
13. [Interfaces](#interfaces)
14. [Embedding](#embedding)
15. [Errors](#errors)
16. [Concurrency](#concurrency)
    * [Goroutines](#goroutines)
    * [Channels](#channels)
    * [Channel Axioms](#channel-axioms)
17. [Printing](#printing)
18. [Reflection](#reflection)
    * [Type Switch](#type-switch)
    * [Examples](https://github.com/a8m/reflect-examples)
19. [Snippets](#snippets)
    * [Files Embedding](#files-embedding)
    * [HTTP Server](#http-server)

## Credits

Most example code taken from [A Tour of Go](http://tour.golang.org/), which is an excellent introduction to Go.
If you're new to Go, do that tour. Seriously.

## Go in a Nutshell

* Imperative language
* Statically typed
* Syntax tokens similar to C (but less parentheses and no semicolons) and the structure to Oberon-2
* Compiles to native code (no JVM)
* No classes, but structs with methods
* Interfaces
* No implementation inheritance. There's [type embedding](http://golang.org/doc/effective%5Fgo.html#embedding), though.
* Functions are first class citizens
* Functions can return multiple values
* Has closures
* Pointers, but not pointer arithmetic
* Built-in concurrency primitives: Goroutines and Channels

# Basic Syntax

## Hello World
File `hello.go`:
```go
package main

import "fmt"

func main() {
    fmt.Println("Hello Go")
}
```
`$ go run hello.go`

## Test
### Command

`go mod init test3`

https://github.com/a8m/golang-cheat-sheet/blob/master/README.md
