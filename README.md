### btcd
---
https://github.com/btcsuite/btcd


```go
// wire/msginv.go
type MsgInv struct {
  InvList []*InvVect
}

func (msg *MsgInv) AddInvVect(iv *InvVect) error {
  if len(msg.InvList)+1 > MaxInvPerMsg {
    str := fmt.Sprintf("too many invvect in message [max %v]",
      MaxInvPerMsg)
    return messageError("MsgInv.AddInvVect", str)
  }
  
  msg.InvList = append(msg.InvList, iv)
  return nil
}



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


