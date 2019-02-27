### authboss
---
https://github.com/volatiletech/authboss

```go
ab := authboss.New()

ab.Config.Storage.Server = myDatabaseImplementation
ab.Config.Storage.SessionState = mySessionImplementation
ab.Config.Storage.CookieState = myCookieImplementation

ab.Config.Paths.Mount = "/authboss"
ab.Config.Paths.RootURL = "https://www.example.com/"

ab.Config.Core.ViewRenderer = abrenderer.New("/auth")

defaults.SetCore(&ab.Config, false)

if err := ab.Init(); err != nil {
  panic(err)
}

mux.Mount("/authboss", http.StripPrefix("/authboss", ab.Config.Core.Router))
```

```
go get -u github.com/volatiletech/authboss
```

```
```


