# studygo

書籍「Go言語によるWebアプリケーション開発」の写経

## Ｇｏのインストール

Mac OSX

`brew install go`

Windows

[ＭＳＩインストーラ](https://golang.org/dl/)

## GOPATH環境変数の設定

```
mkdir $HOME/go
export GOPATH=$HOME/go
export PATH=$PATH:$GOPATH/bin
```

## 外部ライブラリの追加

後述するVisual Studio CodeでGoの拡張機能を入れた時に、あれこれライブラリを入れてと言われるのでここで入れておく。あと`goimports`もついでに入れる。
`go get`したときに、ライブラリを`git clone`してくるものもあるので、事前にgitはインストールしておこう。

```
go get -u -v github.com/nsf/gocode
go get -u -v golang.org/x/tools/cmd/goimports
go get -u -v sourcegraph.com/sqs/goreturns
go get -u -v github.com/tpng/gopkgs
go get -u -v github.com/rogpeppe/godef
go get -u -v github.com/golang/lint/golint
go get -u -v github.com/lukehoban/go-outline
go get -u -v github.com/newhook/go-symbols
go get -u -v golang.org/x/tools/cmd/guru
go get -u -v golang.org/x/tools/cmd/gorename
go get -u -v golang.org/x/tools/cmd/oracle
```

proxy環境下で`go get`ができない場合は、下記環境変数を設定しておく。

```
export http_proxy=http://～
export https_proxy=$http_proxy
```


## 参考

Goプログラミングを始めるにあたって、以下のサイトを参考にさせていただきました。ありがとうございました。
* [The Go Programming Language Documents](http://golang-jp.org/doc/)
* [Go Web プログラミング](https://astaxie.gitbooks.io/build-web-application-with-golang/content/ja/index.html)
* [Visual Studio CodeによるGo言語のデバッグ](http://dev.classmethod.jp/go/visual-studio-code-golang-debug/)
* [Goはクロスコンパイルが簡単](http://unknownplace.org/archives/golang-cross-compiling.html)
