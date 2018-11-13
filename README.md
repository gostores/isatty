# isatty


## Usage

```go
package main

import (
	"fmt"
	"github.com/govenue/isatty"
	"os"
)

func main() {
	if isatty.IsTerminal(os.Stdout.Fd()) {
		fmt.Println("Is Terminal")
	} else if isatty.IsCygwinTerminal(os.Stdout.Fd()) {
		fmt.Println("Is Cygwin/MSYS2 Terminal")
	} else {
		fmt.Println("Is Not Terminal")
	}
}
```

## Installation

```
$ go get github.com/govenue/isatty
```

## License

MIT

## Author

Yasuhiro Matsumoto (a.k.a mattn)
