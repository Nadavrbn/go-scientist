```go
expr := scientist.New("widget-permissions")

expr.Use(func() (interface{}, error) {
  return false, nil
})

expr.Try(func() (interface{}, error) {
  return true, nil
})

expr.Compare(func(control, candidate interface{}) (bool, error) {
  return control == candidate, nil
})

expr.Clean(func(value interface{}) (interface{}, error) {
  return nil, nil
})

expr.Ignore(func(control, candidate interface{}) (bool, error) {
  return false, nil
})

expr.RunIf(func() (bool, error) {

})

expr.SetContext("key", interface{})

value, err := expr.Run()
```
