# Monkeyプログラミング言語

Monkey言語の特徴

* C言語風の構文
* 変数束縛
* 整数と真偽値
* 算術式
* 組み込み関数
* 第一級の高階関数
* クロージャ
* 文字列データ型
* 配列データ型
* ハッシュデータ型

変数の束縛

```cs
let age = 1;
let name = "Monkey";
let result = 10 * (20 / 2);
```

配列とハッシュ

```cs
// 配列
let myArray = [1, 2, 3];
myArray[0] // => 1

// ハッシュ
let thorsten = {"name": "Thorsten", "age", 28};
thorsten["name"] // => Thorsten
```

関数

```cs
let add = fn(a, b) { a + b; };
add(1, 2);
```

高階関数

```cs
let twice = fn(f, x) {
    return f(f(x));
};

let addTwo = fn(x) {
    return x + 2;
};

twice(addTwo, 2);
```
