# 对象池模式

对象池创建模式用于准备和保持多份需求预期的实例。

## 实现

```go
package pool

type Pool chan *Object

func New(total int) *Pool {
	p := make(Pool, total)

	for i := 0; i < total; i++ {
		p <- new(Object)
	}

	return &p
}
```

## 使用

下面是基于对象池的一个简单生命周期例子。

```go
p := pool.New(2)

select {
case obj := <-p:
	obj.Do( /*...*/ )

	p <- obj
default:
	// No more objects left — retry later or fail
	return
}
```

## 经验法则

- 对象池模式适用于当对象初始化的开销大于对象维护开销时。
- 如果对象的需求有尖峰（非平稳型需求），则维护开销可能超过对象池带来的好处。
- 因为对象已经事先创建好了，对象池有性能优势。