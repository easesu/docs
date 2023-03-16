

## 原文

### 原文链接

[The Traversal](https://tinkerpop.apache.org/docs/current/reference/#traversal)

### 原文内容

> At the most general level there is `Traversal<S,E>` which implements `Iterator<E>`, where the S stands for start and the E stands for end. A traversal is composed of four primary components:

> Step<S,E>: an individual function applied to S to yield E. Steps are chained within a traversal.

> TraversalStrategy: interceptor methods to alter the execution of the traversal (e.g. query re-writing).

> TraversalSideEffects: key/value pairs that can be used to store global information about the traversal.

> Traverser<T>: the object propagating through the Traversal currently representing an object of type T.

> The classic notion of a graph traversal is provided by GraphTraversal<S,E> which extends Traversal<S,E>. GraphTraversal provides an interpretation of the graph data in terms of vertices, edges, etc. and thus, a graph traversal DSL.

## 翻译

`Traversal<S,E>`存在于多数常规级别中，`Traversal<S,E>`实现了`Iterator<E>`接口，其中S代表开始，E代表结束。一次遍历由以下四个主要部分组成：

+ `Step<S,E>`: 作用于S并返回E的独立单元，在一次遍历中，多个Step可以链式执行

+ `TraversalStrategy`: 拦截器，用于修改遍历的执行（如 重写查询）

![](images/step-types.png)