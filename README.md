# GORM Oracle driver

## Description
GORM-ORACLE is a GORM driver that does not depend on the Oracle client, Based on [github.com/CengSin/oracle](https://github.com/CengSin/oracle)

### how to install 
```bash
go get github.com/narie-monarie/ora-db
```
### usage
```go
import (
    "gorm.io/gorm"
    oracle "github.com/narie-monarie/ora-db"
    "log"
)

func main(){

    databaseURL := "oracle://username:password@host:port/db"
    db, err := gorm.Open(oracle.Open(databaseURL),&gorm.Config{})
    if err != nil {
        log.Fatal(err)
    }
}
```
