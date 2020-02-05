### btcd
---
https://github.com/btcsuite/btcd


```
```

```sh
go version 
go env GOROOT GOPATH
cd $GOPATH/src/github.com/btcsuite/btcd
GO111MODULE=on go install -v . ./cmd/...
cd $GOPATH/src/github.com/btcsuite/btcd
git pull
GO111MODULE=on go install -v . ./cmd/...
./btcd
```

```
```


