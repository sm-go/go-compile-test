# go-compile-test

### Go Workspace (GOPATH)

There are Three sub directories in Golang Development

- src = contains the source files for your own project
- pkg = contains the go packages, there are non-executbale files or shared libraries ending in (_.a) ($ go get - go mod tidy)
- bin = contains compli

------------

### Go Project Structure

** folder တစ်ခုအတွင်းထဲမှာ package တစ်ခုပဲ ရှိရမယ်။ အခြား package ရှိလို့ မရပါ။ package တစ်ခုကိုမှ file ကြိုက်သလောက်ခွဲလို့ရ၏ (folder ထဲမှာ package တူ, file ကွဲ လို့ ရ၏)
eg. 
 - src (folder)
   |__ server.go (package main)
   |__another.go (package main)

ဒါမျိုး structure ဆိုရင် $ go run folder/*.go နဲ့ run သင့်။
file တစ်ခုနဲ့ တစ်ခု import မလုပ်ပဲ run တဲ့ အခါမျိုးမှာ ( * ) ထည့် run ပါ.
သို့သော် project structure မကျပါ။
Project structure ကျ ဖို့ ဆိုရင် main.go က သီးသန့် ဖြစ်သင့်
$ go run main.go လို့ ဖြစ်သင့်

folder တစ်ခုအတွင်းထဲမှာ package 2 ခု ရှိနေလို့ မရပါ။
eg.
 - src (folder)
   |__ server.go (package main)
   |__another.go (package another)

-----------

### Go CLI

$ go - // is a tool for managing Go source code

$ go run example.go  - // it complies and runs the application

$ go build example.go  - // it just complies the application and produces an executable (./example)

$ go build - // (__.go) it will complies the files in the current directory (./dirname)

$ go build -o app -// will produce an executable file call (./app)

//output binary file in linux

//output exe file in window

------------ 

### GO Compiling

- for Window : GOOS=windows GOARCH=amd64 go build -o winapp.exe
- for Linux : GOOS=linux GOARCH=amd64 go build -o linuxapp
- for Mac : GOOS=darwin GOARCH=amd64 go build -o macapp

$ go install and go build - will compile the package in the current directory
- if the package is main, `go build` will place the resulting executable in the current directory and `go install` will move the executable to GOPATH/bin ($ ls ~/go/bin/) 
// will see executable file with project folder name 
//terminal can call anywhere this package name
- when running go install you use paths relative to GOPATH/src