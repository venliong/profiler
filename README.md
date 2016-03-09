# Profiler

`profiler` is a simple package for mounting the `net/http/pprof` on a chi router.
Just saves a few lines which for chi services to mount a router by:

```go
func MyService() http.Handler {
  r := chi.NewRouter()
  // ..middlewares
  r.Mount("/debug", profiler.Router())
  // ..routes
  return r
}
```
