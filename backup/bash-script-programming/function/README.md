# 函数

## 1 函数定义

shell 中定义函数格式如下:

```shell
[ function ] funname [()] {
  action;

  [return int;]
}
```

> 可以带 function fun() 定义，也可以直接 fun() 定义,不带任何参数。

## 2 函数参数

在 Shell 中，调用函数时可以向其传递参数。在函数体内部，通过 $n 的形式来获取参数的值，例如，$1 表示第一个参数，$2 表示第二个参数... 。

```shell
#!/bin/bash

getFuncParam() {
  for num in $*
  do
    echo "Parameter is $num"
  done
}

getFuncParam 1 2 3 4 5 6 7 8 9 10 11
```

> $10 不能获取第十个参数，获取第十个参数需要${10}。当 n>=10 时，需要使用${n}来获取参数。
