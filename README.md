## fmtags

This is a golang formatting tools


# demo
```go
package main

type Server struct {
    Name        string
    Port        int
    EnableLogs  bool
    BaseDomain  string
    Credentials struct {
        Username string
        Password string
    }
}
```

```shell
$ gomodifytags -file demo.go -struct Server -add-tags json
```

```go
package main

type Server struct {
	Name        string `json:"name"`
	Port        int    `json:"port"`
	EnableLogs  bool   `json:"enable_logs"`
	BaseDomain  string `json:"base_domain"`
	Credentials struct {
		Username string `json:"username"`
		Password string `json:"password"`
	} `json:"credentials"`
}
```

The source code from gomodifytags
