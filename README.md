# Go Cheat Sheet

# Index
1. [Basic Syntax](#basic-syntax)
2. [Tests](#tests)
    * [Command](#command)
3. [Structs](#structs)
4. [Pointers](#pointers)

# Basic Syntax

## Hello World
File `hello.go`:
```
package main

import "fmt"

func main() {
    fmt.Println("Hello Go")
}
```
`$ go run hello.go`

## Tests
### Command

`go mod init test3`

`go test`


```
type person struct {
	firstName string
	lastName  string
}

func main() {
	// alex := person{"Alex", "Anderson"}
	// alex := person{firstName: "Alex", lastName: "Anderson"}

	var alex person

	alex.firstName = "Alex"
	alex.lastName = "Anderson"

	fmt.Println(alex)
	fmt.Printf("%+v", alex)
}
```

# Structs

```
type contactInfo struct {
	email   string
	zipCode int
}

type person struct {
	firstName string
	lastName  string
	// contact   contactInfo
   contactInfo
}

func main() {
	jim := person{
		firstName: "Jim",
		lastName:  "Party",
		contactInfo: contactInfo{
			email:   "jim@gmail.com",
			zipCode: 94000,
		},
	}

	jim.print()
}

func (p person) print() {
	fmt.Printf("%+v", p)
}
```

# Pointers

```
func (pointerToPerson *person) updateName(newFirstName string) {
	(*pointerToPerson ).firstName = newFirstName
}
```

```
jimPointer := &jim
jimPointer.updateName("jimmy")

// jim.updateName("jimmy") will work a shortcut to lines above

jim.print()
```

- &jim is a pointer
- *person is a type pointer to a person
- *pointerToPerson is the value at the address

# Arguments in functions
|Value Types|Reference Types|
|--------|-----------|
|int|slices|
|float|maps|
|string|channels|
|bool|pointers|
|structs|functions|


https://github.com/a8m/golang-cheat-sheet/blob/master/README.md
