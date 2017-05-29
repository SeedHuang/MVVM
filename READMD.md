# 什么是MVVM？仔细拜读了一下wiki，给到的答案十非简洁

## M
M就是Model，你可以理解为一个Domain Model，或者个数据访问层，反正就是数据

## V
V就是View，View层就是最后呈现在屏幕上的视图结构或者说是布局。

## VM
VM就是ViewModel，他是数据的状态，用以串联视图与数据，举个例子：
假设你有以下的数据结构
```
{
    error: 0,
    data: {
        name: "Huagnchunhua",
        age: "32"
    }
}
```

这是一个目标数据，但是你一开始其实拿的不一定是这个数据，因为比如
```
{
    error: 10220:
    data: "参数错误"
}

{
    error: 1:
    data: null
}
```
所应对error不同状态，会有对应的View展现，数据错误的和没有数据的视图
