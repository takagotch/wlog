### wlog
---
https://github.com/influxdata/wlog

```go
package main

import (
  "log"
  "os"
  
  "github.com/influxdata/wlog"
)

func main() {
  var logger *log.Logger
  logger = wlog.New(os.Stderr, "prefix", log.LstdFlags)
  logger.Println("I! initialized logger")
}

package main

import (
  "log"
  "os"
  
  "github.com/influxdata/wlog"
)

func main() {
  var logger *log.Logger
  logger = log.New(wlog.NewWriter(os.Stderr), "prefix", log.LstdFlags)
  logger.Println("I! initialized logger")
}

package main

import (
  "log"
  "os"
  
  "github.com/influxdata/wlog"
)

func main() {
  var logger *log.Logger
  logger = wlog.New(os.Stderr, "prefix", log.LstdFlags)
  wlog.SetLevel(wlog.DEBUG)
  logger.Println("D! this message will be drpped")
  logger.Println("I! this message will be printed")
}
```

```
```

```
```


