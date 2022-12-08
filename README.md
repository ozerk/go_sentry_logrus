# go_sentry_logrus

## Usage

```
package main

import (
	sentryLogrus "github.com/ozerk/go_sentry_logrus"
	"os"
)

func main() {
	sentryLogrus.LoggerInit(os.Getenv("SENTRY_DSN"))
	database, err := gorm.Open(postgres.Open(dbURL), &gorm.Config{Logger: sentryLogrus.NewGormLog()})
}
```