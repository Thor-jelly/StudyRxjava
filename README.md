# StudyRxjava

> 学习自简书Carson_Ho的[Android RxJava：这是一份全面 & 详细 的RxJava操作符 使用攻略](https://www.jianshu.com/p/cd984dd5aae8)  
> gitbook[官方翻译](https://mcxiaoke.gitbooks.io/rxdocs/content/)

## [创建操作符](https://github.com/Thor-jelly/StudyRxjava/blob/master/%E5%88%9B%E5%BB%BA%E6%93%8D%E4%BD%9C%E7%AC%A6.md)  

```
        creat;
        just;//快速创建对象，最多发送十个对象
        fromArray;//数组遍历
        fromIterable;//遍历
        empty;//仅发送Complete事件，直接通知完成
        error;//仅发送Error事件，直接通知异常
        never;//不发送任何事件
        defer;//直到有观察者observer订阅时，才动态创建被观察者对象 并 发送事件
        timer;//延迟指定时间后，调用一次onNext(0)
        interval;//每隔指定事件发送事件，无限叠加发送，从0开始
        intervalRange;//每隔指定时间 就发送事件，并指定发送事件数量
        range;//连续发送一个事件序列，可指定次数
```

## [变换操作符](https://github.com/Thor-jelly/StudyRxjava/blob/master/%E5%8F%98%E6%8D%A2%E6%93%8D%E4%BD%9C%E7%AC%A6.md)

```
        map;//数据转换
        flatMap;//将被观察者发送的事件序列进行拆分，并且单独转换，再合并成一个新的事件序列，最后进行发送
        concatMap;//类似FlatMap（）操作符;区别：拆分并且重新合并生成的事件序列的顺序 等于 被观察者旧序列生产的顺序
        buffer;//缓存区大小 = 每次从被观察者中获取的事件数量, 步长 = 从当前位置向后移动几位
```

## [组合/合并操作符](https://github.com/Thor-jelly/StudyRxjava/blob/master/%E7%BB%84%E5%90%88-%E5%90%88%E5%B9%B6%E6%93%8D%E4%BD%9C%E7%AC%A6.md)

```
        concat;//concat组合被观察者数量<=4,顺序执行
        concatArray;//concatArray组合观察者数量>4,顺序执行
        merge;//组合被观察者数量<=4,非顺序执行
        mergeArray;//组合被观察者数量>4,非顺序执行
        concatArrayDelayError;//第1个被观察者的Error事件将在第2个被观察者发送完事件后再继续发送,mergeDelayError（）操作符同理
        mergeDelayError;
        zip;//严格按照原先事件序列 进行对位合并,最终合并的事件数量 = 多个被观察者（Observable）中数量最少的数量
        combineLatest;//当两个Observables中的任何一个发送了数据后，将先发送了数据的Observables 的最新（最后）一个数据
                        与 另外一个Observable发送的每个数据结合，最终基于该函数的结果发送数据,与reduce区别就是接收的事件是每次都有而reduce只有最                        后一次输出信息
        reduce;//把前2个数据聚合，然后与后1个数据继续进行聚合，依次类推
        collect;//将被观察者Observable发送的数据事件收集到一个数据结构里
        startWith;//在一个被观察者发送事件前，追加发送一些数据/ 一个新的被观察者, 后调用的startWith先追加
        startWithArray;
        count;//统计被观察者发送事件的数量
```

## [功能性操作符](https://github.com/Thor-jelly/StudyRxjava/blob/master/%E5%8A%9F%E8%83%BD%E6%80%A7%E6%93%8D%E4%BD%9C%E7%AC%A6.md)  

```
        delay;//指定延迟时间
        do;//在某个事件的生命周期中调用
        retry;//重试，即出现错误，让被观察者重新发送数据
        retryWhen;//出现错误后，判断是否需要重新发送数据
        repeat;//重复不断地发送被观察者事件
        repeatWhen;//有条件地、重复发送 被观察者事件
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
