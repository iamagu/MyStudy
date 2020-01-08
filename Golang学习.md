# Go语法学习
## 变量
1. 匿名变量`_`
2. 局变量
3. 全局变量
    1. 必须以var定义
    2. 同包可访问全局变量，直接使用变量名访问
    3. 跨包可访问全局变量
        1. 变量名必须大写字母开头
        2. import变量源文件所在包，以`包名.变量名`访问
## 数据类型
1. 数值类型
    1. 整数：int8/unit8, int16/unit16, int32/unit32, int64/unit64, int/unit, byte, rune
    2. 浮点数
    3. 复数

2. 字符串
    1. 带转义的字符串，使用`""`包围
    2. 不带转义的字符串，使用` `` `

3. 字符
    1. byte
    2. rune

## 流程控制
1. if分支
2. switch分支
    1. case多条件
        switch {
        case "a", "b", "c":
            // do something
        default:
            // do default thing
        }

    2. case条件表达式
        switch {
        case 1>0 & 2> 3:
            // do something
        default:
            // do default thing
        }

    3. fallthrough,无条件执行下一个case

3. for循环
    完整格式
    for <初始语句>; <执行条件表达式>; <执行后语句> {
        // do something
    }
    
    无限循环
    for {
        // do something
    }
    
    只有条件
    for <执行条件表达式> {
        // do something
    }
    
    跳出循环
    break、goto、return、panic
    
    for range循环（键值循环）：数组、切片、字符串、map、通道
    for key, val := range coll {
        // do something
    }
