# go-pagerduty

PagerDuty API client in Go.

Tested on all Go versions 1.0 and higher.

## Getting started

```go
package main

import "fmt"
import "github.com/danryan/go-pagerduty/pagerduty"

func main() {
  subdomain := "PAGERDUTY_SUBDOMAIN"
  apiKey := "PAGERDUTY_API_KEY"
  pd := pagerduty.New(subdomain, apiKey)

  incident := pd.Incidents.Get("ABCDEF")

  fmt.Printf("incident %v: status: %v\n", incident.ID, incident.Status)
}
```

## Resources

* [API documentation](http://godoc.org/github.com/danryan/go-pagerduty)
* [Bugs, questions, and feature requests](https://github.com/danryan/hal/issues)

## Is it any good?

[Possibly.](http://news.ycombinator.com/item?id=3067434)

## License

This library is distributed under the MIT License, a copy of which can be found in the [LICENSE](LICENSE) file.
