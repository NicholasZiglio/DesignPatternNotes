# Design Patterns

## Creational
Creational design patterns provide various object creation mechanisms, which increase flexibility and reuse of existing code.

### Factory Method
Delegates object creation to subclasses of a designated factory class that produce a different type. All objects are created through a common interface used by clients which remain unaware of concrete type used, promoting loose coupling.

### Abstract Factory
Delegates creation of multiple objects to guarantee they all belong to the same family of objects. Each subclass of the factory class will return a different family type of object. All objects are created through common interfaces used by clients which remain unaware of concrete family type used, promoting loose coupling.

### Builder
Simplifies complex construction by delegating responsibility to new builder object that breaks down construction into steps. Steps can be called by builder object or a new director objects that can further customize which steps to call and their order.

### Prototype
Implement clone method to create a new duplicate instance of an object.

### Singleton (Antipattern)
Enforces only one instance of an object. Private constructure public static getter.
Antipattern because:
- Introduces global state
- Tight coupling with code that uses it
- Concurrency issues
- Difficulties testing
- etc..

## Structural
Structural design patterns explain how to assemble objects and classes into larger structures, while keeping these structures flexible and efficient.


### Adapter
Object that implements an existing client compatible interface by adapting the existing incompatible interface of a contained object.

### Bridge
Abstraction and implementation are separated. Client interacts with abstraction which contains instance of implementation interface so that it can vary (loose coupling).

### Composite
Single interface to allow objects of the same interface to form parent-child relationships and form a tree like structure.

### Decorator
Adds behavior to objects dynamically by wrapping them (using composition). Can add behaviour before and after calling the wrapped object's original behaviour.

### Facade
Provides a new simple unified interface to a complex system.

### Flyweight
Optimizes memory usage by sharing a single instance of an object across multiple similar objects, which would otherwise duplicate its data. Contains shared (intrinsic) state and receives unique (extrinsic) state.

### Proxy
Contains an object and implements same interface to create a level of indirection and manage the interaction with the actual object. Enables lazy initialization, security checks, logging requests, caching results, etc. without changing the existing code of the real object.


## Behavioural
Behavioral design patterns are concerned with algorithms and the assignment of responsibilities between objects.


### Chain of Responsibility
Request defined in common interface is passed along a chain of objects that can potentially handle the request. The chain of objects is usually implemented by composition (often using an already existing composite) but could also be centralized in a manager object that implements the chain's data structure.

### Command
Encapsulates a request as an object implementing interface containing execute and undo methods. This transformation lets you pass requests as a method arguments, delay or queue a request’s execution, and support undoable operations.

### Iterator
Implements interface with next and has next methods to traverse a collection without exposing its structure. Can be implemented as a separate class (also using visitor pattern), or can be implemented in collection class itslef.

### Mediator
Reduces interactions between objects by forcing them to collaborate only via a mediator object.

### Memento
Save and restore the previous state of an object without revealing the details of its implementation.

### Observer
Call functionality of multiple subscribing objects (via a delegate function) when an event is invoked from publisher object.

### State
 The base state class implements the state interface by delegating behavior to a contained state subclass. Each state subclass, in turn, implements the state interface with specific behavior. By swapping the type of state subclass it contains, the state base class can dynamically alter its behavior.

### Strategy
Define a family of algorithms by putting each of them into separate interchangeable classes that implement the same interface with execute method.

### Template Method
Defines and implements the skeleton of an algorithm in the superclass but lets subclasses override specific steps of the algorithm without changing its structure.

### Visitor
 A visitor interface declares operations that can be performed on elements of a data structure. Concrete visitor classes implement these operations. Elements of the data structure implement an accept method, which take the visitor interface as an argument and delegates the operation to the visitor. This enables applying different behaviors to elements without altering their classes.
