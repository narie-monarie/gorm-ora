# GORM Oracle driver

## Description
GORM-ORACLE is a GORM driver that does not depend on the Oracle client, Based on [github.com/CengSin/oracle](https://github.com/CengSin/oracle)
, not thoroughly tested and not recommended for production use.

## DB Driver
[go-ora](https://github.com/sijms/go-ora)
A pure golang development of Oracle driver, do not need to install Oracle client.

## Quick Start
### how to install 
```bash
go get github.com/wdrabbit/gorm-oracle
```
### usage
```go
import (
    "gorm.io/gorm"
    "oracle "github.com/narie-monarie/ora-db"
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
