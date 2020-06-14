# Go言語でつくるインタプリタ

> 本書は、Go言語でプログラミング言語のインタプリタを作りながら、プログラミング言語とそのインタプリタについて学ぶ書籍です。
> 順を追ってコードを示し、C言語風の構文を持つ言語「Monkeyプログラミング言語」のインタプリタを組み立てていきます。字句解析器、構文解析器、評価器を作りながら、ソースコードをトークン列に、トークン列を抽象構文木に変換し、その抽象構文木を評価し実行する方法を学びます。さらに、インタプリタに新しいデータ型を導入し、組み込み関数を追加して、言語を拡張していきます。付録では構文マクロシステムについても扱います。
> 本書では、Go言語標準のツールキット以外のサードパーティライブラリやフレームワークは使用せず、0行のコードからはじめて、完動するインタプリタができあがるところまでを体験します。その過程を通じて、プログラミング言語とインタプリタの仕組みを実践的に学ぶことができます。

## TOC

大きく分けて次の4つから構成されている。

1. 字句解析
2. 構文解析
3. 評価
4. インタプリタの拡張

## repl
sample
```go
$ go run main.go 
Hello hoge! This is the Monkey programming language!
Feel free to type in commands
>> let add = fn(x, y) { x + y; };  
{Type:LET Literal:let}
{Type:IDENT Literal:add}
{Type:= Literal:=}
{Type:FUNCTION Literal:fn}
{Type:( Literal:(}
{Type:IDENT Literal:x}
{Type:, Literal:,}
{Type:IDENT Literal:y}
{Type:) Literal:)}
{Type:{ Literal:{}
{Type:IDENT Literal:x}
{Type:+ Literal:+}
{Type:IDENT Literal:y}
{Type:; Literal:;}
{Type:} Literal:}}
{Type:; Literal:;}
```
