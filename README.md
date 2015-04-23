Random.org Client Library for Golang
------------------------------------

This is a client used to access random.org using their JSON-RPC interface. It
provides the 'basic' random generation functions.

It is basically a prototype/POC, but it does work.

Example:
<pre>
package main

import (
        "fmt"
        "github.com/jamesunger/rdoclient"
)

func main() {
        myints,err := rdoclient.GenerateIntegers("APIKEY",1,1,8,true)
        if err != nil {
                fmt.Println("Failed to get integers: ", err)
                return
        }

        fmt.Println("Hi", myints[0])
}
</pre>
