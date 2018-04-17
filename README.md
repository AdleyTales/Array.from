## 前言：为什么写这个?：
> Array.from() 非常方便的将一个类数组的集合 ==》 数组，直接使用数组身上的方法。例如：常用的map，foreach...
> 但是，问题来了，IE不识别Array.from这个方法。所以写了它兼容IE的写法。

## 兼容代码写法如下：

```
if(!Array.from){
    Array.from = function (el) {
	return Array.apply(this, el);
    }
}
```
