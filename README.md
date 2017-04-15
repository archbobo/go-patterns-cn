<p align="center">
  <img src="/gopher.png" height="400">
  <h1 align="center">
    Go Patterns
  </h1>
</p>

一堆Go语言惯例和应用模式，翻译自[go patterns](http://tmrts.com/go-patterns)，翻译目的主要是为了自己学习go语言。

## 创建模式

| 模式 | 描述 | 状态 |
|:-------:|:----------- |:------:|
| [抽象工厂Abstract Factory](/creational/abstract_factory.md) | 一个用于创建相关对象族的接口 | ✘ |
| [构建器Builder](/creational/builder.md) | 利用简单对象构建一个复杂对象 | ✔ |
| [工厂方法Factory Method](/creational/factory.md) | 将对象创建工作推迟委派给一个指定的函数 | ✔ |
| [对象池Object Pool](/creational/object-pool.md) | 实例化并维护一组相同类型的对象实例 | ✔ |
| [单例Singleton](/creational/singleton.md) | 限制只能实例化一个对象 | ✔ |

## 结构模式

| 模式 | 描述 | 状态 |
|:-------:|:----------- |:------:|
| [Bridge](/structural/bridge.md) | Decouples an interface from its implementation so that the two can vary independently | ✘ |
| [Composite](/structural/composite.md) | Encapsulates and provides access to a number of different objects | ✘ |
| [Decorator](/structural/decorator.md) | Adds behavior to an object, statically or dynamically | ✔ |
| [Facade](/structural/facade.md) | Uses one type as an API to a number of others | ✘ |
| [Flyweight](/structural/flyweight.md) | Reuses existing instances of objects with similar/identical state to minimize resource usage | ✘ |
| [Proxy](/structural/proxy.md) | Provides a surrogate for an object to control it's actions | ✘ |

## 行为模式

| 模式 | 描述 | 状态 |
|:-------:|:----------- |:------:|
| [Chain of Responsibility](/behavioral/chain_of_responsibility.md) | Avoids coupling a sender to receiver by giving more than object a chance to handle the request | ✘ |
| [Command](/behavioral/command.md) | Bundles a command and arguments to call later | ✘ |
| [Mediator](/behavioral/mediator.md) | Connects objects and acts as a proxy | ✘ |
| [Memento](/behavioral/memento.md) | Generate an opaque token that can be used to go back to a previous state | ✘ |
| [Observer](/behavioral/observer.md) | Provide a callback for notification of events/changes to data | ✔ |
| [Registry](/behavioral/registry.md) | Keep track of all subclasses of a given class | ✘ |
| [State](/behavioral/state.md) | Encapsulates varying behavior for the same object based on its internal state | ✘ |
| [Strategy](/behavioral/strategy.md) | Enables an algorithm's behavior to be selected at runtime | ✔ |
| [Template](/behavioral/template.md) | Defines a skeleton class which defers some methods to subclasses | ✘ |
| [Visitor](/behavioral/visitor.md) | Separates an algorithm from an object on which it operates | ✘ |

## 同步模式

| 模式 | 描述 | 状态 |
|:-------:|:----------- |:------:|
| [Condition Variable](/synchronization/condition_variable.md) | Provides a mechanism for threads to temporarily give up access in order to wait for some condition | ✘ |
| [Lock/Mutex](/synchronization/mutex.md) | Enforces mutual exclusion limit on a resource to gain exclusive access | ✘ |
| [Monitor](/synchronization/monitor.md) | Combination of mutex and condition variable patterns | ✘ |
| [Read-Write Lock](/synchronization/read_write_lock.md) | Allows parallel read access, but only exclusive access on write operations to a resource | ✘ |
| [Semaphore](/synchronization/semaphore.md) | Allows controlling access to a common resource | ✔ |

## 并发模式

| 模式 | 描述 | 状态 |
|:-------:|:----------- |:------:|
| [N-Barrier](/concurrency/barrier.md) | Prevents a process from proceeding until all N processes reach to the barrier | ✘ |
| [Bounded Parallelism](/concurrency/bounded_parallelism.md) | Completes large number of independent tasks with resource limits | ✔ |
| [Broadcast](/concurrency/broadcast.md) | Transfers a message to all recipients simultaneously | ✘ |
| [Coroutines](/concurrency/coroutine.md) | Subroutines that allow suspending and resuming execution at certain locations | ✘ |
| [Generators](/concurrency/generator.md) | Yields a sequence of values one at a time | ✔ |
| [Reactor](/concurrency/reactor.md) | Demultiplexes service requests delivered concurrently to a service handler and dispatches them syncronously to the associated request handlers | ✘ |
| [Parallelism](/concurrency/parallelism.md) | Completes large number of independent tasks | ✔ |
| [Producer Consumer](/concurrency/producer_consumer.md) | Separates tasks from task executions | ✘ |

## 消息模式

| 模式 | 描述 | 状态 |
|:-------:|:----------- |:------:|
| [Fan-In](/messaging/fan_in.md) | Funnels tasks to a work sink (e.g. server) | ✔ |
| [Fan-Out](/messaging/fan_out.md) | Distributes tasks among workers (e.g. producer) | ✔ |
| [Futures & Promises](/messaging/futures_promises.md) | Acts as a place-holder of a result that is initially unknown for synchronization purposes | ✘ |
| [Publish/Subscribe](/messaging/publish_subscribe.md) | Passes information to a collection of recipients who subscribed to a topic | ✔ |
| [Push & Pull](/messaging/push_pull.md) | Distributes messages to multiple workers, arranged in a pipeline | ✘ |

## 稳定性模式

| 模式 | 描述 | 状态 |
|:-------:|:----------- |:------:|
| [Bulkheads](/stability/bulkhead.md)  | Enforces a principle of failure containment (i.e. prevents cascading failures) | ✘ |
| [Circuit-Breaker](/stability/circuit-breaker.md) | Stops the flow of the requests when requests are likely to fail | ✔ |
| [Deadline](/stability/deadline.md) | Allows clients to stop waiting for a response once the probability of response becomes low (e.g. after waiting 10 seconds for a page refresh) | ✘ |
| [Fail-Fast](/stability/fail_fast.md) | Checks the availability of required resources at the start of a request and fails if the requirements are not satisfied | ✘ |
| [Handshaking](/stability/handshaking.md) | Asks a component if it can take any more load, if it can't, the request is declined | ✘ |
| [Steady-State](/stability/steady_state.md) | For every service that accumulates a resource, some other service must recycle that resource | ✘ |

## 探测模式

| 模式 | 描述 | 状态 |
|:-------:|:----------- |:------:|
| [Timing Functions](/profiling/timing.md) | Wraps a function and logs the execution | ✔ |

## 惯例

| 模式 | 描述 | 状态 |
|:-------:|:----------- |:------:|
| [Functional Options](/idiom/functional-options.md) | Allows creating clean APIs with sane defaults and idiomatic overrides | ✔ |

## 反模式

| 模式 | 描述 | 状态 |
|:-------:|:----------- |:------:|
| [Cascading Failures](/anti-patterns/cascading_failures.md) | A failure in a system of interconnected parts in which the failure of a part causes a domino effect | ✘ |