# MacでのC#開発環境の設定

## 手順

### C#のコンパイラ(Mono)をインストール

 Mono(https://www.mono-project.com/docs/getting-started/mono-basics/)
> Mono, the open source development platform based on the .NET Framework, allows developers to build cross-platform applications with improved developer productivity.
> C# Compiler - Mono’s C# compiler is feature complete for C# 1.0, 2.0, 3.0, 4.0 and 5.0 (ECMA). A  good description of the feature of the various versions is available on Wikipedia. 

* ```brew install mono```

### コードをかく

* touch main.cs
* code main.cs

```using System;
public class MonoSample
{
    static public void Main ()
    {
        Console.WriteLine ("Hello Mono World");
    }
}
```

### コンパイルと＋実行

__mcs:コンパイルコマンド
mono:実行コマンド__

* mcs main.cs
* mono main.exe

### 複数ファイルのコンパイル

* mcs hello1.cs hello2.cs -out:hello.exe
* mcs *.cs -out:hello.exe

### 参考にしたサイト

* https://qiita.com/matsuda_sinsuke/items/76068f4c396887459803