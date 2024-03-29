[![GoDoc](https://godoc.org/github.com/beeva-labs/text-tokenizer?status.svg)](https://godoc.org/github.com/beeva-labs/text-tokenizer)
[![Build Status](https://travis-ci.org/beeva-labs/text-tokenizer.svg?branch=master)](https://travis-ci.org/beeva-labs/text-tokenizer)
[![Go Report Card](https://goreportcard.com/badge/github.com/beeva-labs/text-tokenizer)](https://goreportcard.com/report/github.com/beeva-labs/text-tokenizer)

# text tokenizer
Simple rule-based word/sentence tokenizer.

## Installation
```bash
go install github.com/beeva-labs/text-tokenizer
```

## Demo
````go
package main

import (
	"fmt"
	"github.com/beeva-labs/text-tokenizer"
)

func main() {
	var input string = `Go (often referred to as golang) is a programming language created at Google[12] in 2.009 by Robert Griesemer, Rob Pike, and Ken Thompson[10]. It is a compiled, statically typed language in the tradition of Algol and C, with garbage collection, limited structural typing[3], memory safety features and CSP-style concurrent programming features added.`

	var sentences []string = tokenizer.Sentences(input)
	for _, s := range sentences {
		fmt.Printf("%q\n", tokenizer.Words(s))
	}
}
````