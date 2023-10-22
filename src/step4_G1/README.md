# 設計

## 関数型プログラミング

オブジェクト指向プログラミングではなく、関数型プログラミングを採用しています。
すべてのメソッドは副作用を持たない静的メソッドです。
関数型プログラミングによって、プログラムのテストが容易になります。

### 副作用

副作用とは、関数の実行によって、関数の外部に影響を与えることです。
副作用を持つ関数は、同じ引数を与えても、異なる結果を返すことがあります。

### 静的メソッド

静的メソッドとは、オブジェクトを生成せずに呼び出すことができるメソッドです。

# print メソッド

## 概要

print メソッドは、引数に指定した文字列を標準出力に出力します。

## 引数

| 引数名 | 型 | 説明 |
|:--|:--|:--|
| message | String | 表示する文字列 |

## 戻り値

なし

## 使い方

```java
public class Main {
    public static void main(String[] args) {
        print("Hello, World!");
    }
}
```

## 標準出力結果

```
Hello, World!
```

# println メソッド

## 概要

println メソッドは、引数に指定した文字列を標準出力に出力します。出力後に改行を行います。

## 引数

| 引数名 | 型 | 説明 |
|:--|:--|:--|
| message | String | 表示する文字列 |

## 戻り値

なし

## 使い方

```java
public class Main {
    public static void main(String[] args) {
        println("Hello, World!");
    }
}
```

## 標準出力結果

```
Hello, World!
```

# print メソッドと println メソッドの違い

print メソッドは、引数に指定した文字列を標準出力に出力します。出力後に改行を行いません。

# main メソッド

## 概要

main メソッドは、Java アプリケーションのエントリーポイントです。Java アプリケーションは、main メソッドから実行されます。

## 引数

| 引数名 | 型 | 説明 |
|:--|:--|:--|
| args | String[] | コマンドライン引数 |

## 戻り値

なし

## 使い方

```java

public class Main {
    public static void main(String[] args) {
        println("Hello, World!");
    }
}
```

## 標準出力結果

```
Hello, World!
```

## コマンドライン引数

コマンドライン引数は、Java アプリケーションを実行する際に指定することができる引数です。コマンドライン引数は、main メソッドの引数に渡されます。

# calcAve メソッド

## 概要

calcAve メソッドは、引数に指定した数値の平均値を計算します。

## 式

$$
\frac{1}{n} \sum_{i=1}^{n} numbers_i
$$

## 引数

| 引数名 | 型 | 説明 |
|:--|:--|:--|
| numbers | double[] | 入力されたデータ |

## 戻り値

| 戻り値の型 | 説明 |
|:--|:--|
| double | 平均値 |

## 使い方

```java
public class Main {
    public static void main(String[] args) {
        double[] numbers = { 1, 2, 3, 4, 5 };
        double average = calcAve(numbers);
        println(average);
    }
}
```

## 標準出力結果

```
3.0
```

# calcMax メソッド

## 概要

calcMax メソッドは、引数に指定した数値の最大値を計算します。

## 式

$$
\max numbers
$$

## 引数

| 引数名 | 型 | 説明 |
|:--|:--|:--|
| numbers | double[] | 入力されたデータ |

## 戻り値

| 戻り値の型 | 説明 |
|:--|:--|
| double | 最大値 |

## 使い方

```java
public class Main {
    public static void main(String[] args) {
        double[] numbers = { 1, 2, 3, 4, 5 };
        double max = calcMax(numbers);
        println(max);
    }
}
```

## 標準出力結果

```
5.0
```

# calcMin メソッド

## 概要

calcMin メソッドは、引数に指定した数値の最小値を計算します。

## 式

$$
\min numbers
$$

## 引数

| 引数名 | 型 | 説明 |
|:--|:--|:--|
| numbers | double[] | 入力されたデータ |

## 戻り値

| 戻り値の型 | 説明 |
|:--|:--|
| double | 最小値 |

## 使い方

```java
public class Main {
    public static void main(String[] args) {
        double[] numbers = { 1, 2, 3, 4, 5 };
        double min = calcMin(numbers);
        println(min);
    }
}
```

## 標準出力結果

```
1.0
```

# calcStd メソッド

## 概要

calcStd メソッドは、引数に指定した数値の標準偏差を計算します。

## 式

$$
\sqrt{\frac{1}{n} \sum_{i=1}^{n} (numbers_i - \bar{numbers})^2}
$$

## 引数

| 引数名 | 型 | 説明 |
|:--|:--|:--|
| numbers | double[] | 入力されたデータ |

## 戻り値

| 戻り値の型 | 説明 |
|:--|:--|
| double | 標準偏差 |

## 使い方

```java
public class Main {
    public static void main(String[] args) {
        double[] numbers = { 1, 2, 3, 4, 5 };
        double std = calcStd(numbers);
        println(std);
    }
}
```

## 標準出力結果

```
1.4142135623730951
```

# disp メソッド

## 概要

disp メソッドは、統計データを標準出力に出力します。
最大値、最小値、平均値、標準偏差を出力します。

## 引数

| 引数名 | 型 | 説明 |
|:--|:--|:--|
| title | String | 統計のタイトル |
| numbers | double[] | 入力されたデータ |

## 戻り値

なし

## 使い方

```java
public class Main {
    public static void main(String[] args) {
        double[] numbers = { 1, 2, 3, 4, 5 };
        disp("Sample", numbers);
    }
}
```

## 標準出力結果

```
***** Sample *****
最大値 = 5.0
最小値 = 1.0
平均値 = 3.0
標準偏差 = 1.4142135623730951
```

# runTest メソッド

## 概要

runTest メソッドは、すべてのメソッドが正しいかどうかをテストします。

## 引数

なし

## 戻り値

なし

## 使い方

```java
public class Main {
    public static void main(String[] args) {
        runTest();
    }
}
```

## 標準出力結果

```
OK: 平均
OK: 最大値
OK: 最小値
OK: 標準偏差
```

# assertEqual メソッド

## 概要

assertEqual メソッドは、2 つの値が等しいかどうかをテストします。
正しければ OK と表示します。
間違っていれば NG と表示して、期待値と実際の値を表示します。

## 引数

| 引数名 | 型 | 説明 |
|:--|:--|:--|
| message | String | テストのタイトル |
| expected | double | 期待値 |
| actual | double | 実測値 |

## 戻り値

なし

## 使い方

```java
public class Main {
    public static void main(String[] args) {
        assertEqual("1", 3.0, 3.0);
        assertEqual("2", 3.0, 4.0);
    }
}
```

## 標準出力結果

```
OK: 1
NG: 2
  期待: 3.0
  実際: 4.0
```