Cache
================================
Simple in memory cache implementation.

See it in action:

```go
package main

import (
	"fmt"

	"github.com/khabirovar/cache"
)

func main() {
	cache := cache.New()

	cache.Set("userId", 42)
	userId := cache.Get("userId")

	fmt.Println(userId)

	cache.Delete("userId")
	userId := cache.Get("userId")

	fmt.Println(userId)
}
```