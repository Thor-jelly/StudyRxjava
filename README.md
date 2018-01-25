# StudyRxjava

> 学习自简书Carson_Ho的[Android RxJava：这是一份全面 & 详细 的RxJava操作符 使用攻略](https://www.jianshu.com/p/cd984dd5aae8)  
> gitbook[官方翻译](https://mcxiaoke.gitbooks.io/rxdocs/content/)

## [创建操作符](https://github.com/Thor-jelly/StudyRxjava/blob/master/%E5%88%9B%E5%BB%BA%E6%93%8D%E4%BD%9C%E7%AC%A6.md)

```
        creat;
        just;
        fromArray;
        fromIterable;
        empty;
        error;
        never;
        defer;
        timer;
        interval;
        intervalRange;
        range;
```        

## [变换操作符](https://github.com/Thor-jelly/StudyRxjava/blob/master/%E5%8F%98%E6%8D%A2%E6%93%8D%E4%BD%9C%E7%AC%A6.md)

```
        map;
        flatMap;
        concatMap;
        buffer;
```

## [组合/合并操作符](https://github.com/Thor-jelly/StudyRxjava/blob/master/%E7%BB%84%E5%90%88-%E5%90%88%E5%B9%B6%E6%93%8D%E4%BD%9C%E7%AC%A6.md)

```
        concat;
        concatArray;
        merge;
        mergeArray;
        concat;
        concatArrayDelayError;
        mergeDelayError;
        zip;
        combineLatest;
        reduce;
        collect;
        startWith;
        startWithArray;
        count;
```

## [功能性操作符](https://github.com/Thor-jelly/StudyRxjava/blob/master/%E5%8A%9F%E8%83%BD%E6%80%A7%E6%93%8D%E4%BD%9C%E7%AC%A6.md)  

```
        delay;
        do;
        retry;
        retryWhen;
        repeat;
        repeatWhen;
```

## [过滤操作符](https://github.com/Thor-jelly/StudyRxjava/blob/master/%E8%BF%87%E6%BB%A4%E6%93%8D%E4%BD%9C%E7%AC%A6.md)

```
        filter；过滤 特定条件的事件
        ofType；过滤 特定类型的数据
        skip；跳过指定事件，也可跳过指定时间时间
        skipLast；跳过指定最后事件，也可跳过最后时间时间
        distinct；去重
        distinctUntilChanged；连续重复才去重
        take；接收事件数量
        takeLast；只接收最后几个事件数量
        throttleFirst；指定时间内只接收第一次事件
        throttleLast/sample；指定时间内只接收最后一次次事件
        throttleWithTimeout／debounce；采样频率，指定时间只接收最新事件
        firstElement；//获取第一个事件
        lastElement；//获取最后一个事件
        elementAt；//获取指定位置事件，如果超出位置没有任何提示，如果需要提示则调用elementAtOrError()，如超出位置需要指定默认值则调用elementAt 2个参数的方法
```
