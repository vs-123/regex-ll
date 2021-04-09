# regex-ll

![regex-ll](https://raw.githubusercontent.com/vs-123/regex-ll/main/icon.png?token=AES3AMUGTHELZO6JW4YE5CDAOACOG)

## Introduction:
**regex-ll** is a lined-language that was designed for testing your regular expressions on the fly.

## Quick Start:
Suppose, I want to test this regular expression `([0-9])` with substitutions.
So I would create a file `main.ll` (the file name is arbitrary).
In `main.ll`, I would write the following code.
```
regex ([0-9])
string "1234567890"
substitute "A$1 "
show
```
Output:
```
$ ./regex-ll main.ll
regex pattern: ([0-9])
string: 1234567890
match: true
substitution: A1 A2 A3 A4 A5 A6 A7 A8 A9 A0
```
For now (since 9 April 2021), there are only four commands:-

 - `regex <regular expression>`
 - `string "<string to perform match/substitution on>"`
 - `substitute "<substitution>"`
 - `show`

