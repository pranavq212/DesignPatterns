# DesignPatterns
GOF The four authors Erich Gamma, Richard Helm, Ralph Johnson and John Vlissides are collectively introduced Gang of Four Design Patterns in Software development. In 1994, they published a book (Design Patterns: Elements of Reusable Object-Oriented Software) for explaining the concept of Design Patterns.
1. Creational Patterns

  Abstract Factory
Creates an instance of several families of classes

  Builder
Separates object construction from its representation

  Factory Method
Creates an instance of several derived classes

  Prototype
A fully initialized instance to be copied or cloned

  Singleton
A class of which only a single instance can exist

2. Structural Patterns

  Adapter
Match interfaces of different classes

  Bridge
Separates an object’s interface from its implementation

  Composite
A tree structure of simple and composite objects

  Decorator
Add responsibilities to objects dynamically

  Facade
A single class that represents an entire subsystem

  Flyweight
A fine-grained instance used for efficient sharing

  Proxy
An object representing another object

3. Behavioral Patterns

  Chain of Resp.
A way of passing a request between a chain of objects

  Command
Encapsulate a command request as an object

  Interpreter
A way to include language elements in a program

  Iterator
Sequentially access the elements of a collection

  Mediator
Defines simplified communication between classes

  Memento
Capture and restore an object's internal state

  Observer
A way of notifying change to a number of classes

  State
Alter an object's behavior when its state changes

  Strategy
Encapsulates an algorithm inside a class

  Template Method
Defer the exact steps of an algorithm to a subclass

  Visitor
Defines a new operation to a class without change

Factory vs Abstract Factory
Both Abstract Factory and Factory design pattern are creational design pattern and use to decouple clients from creating object they need, But there is a significant difference between Factory and Abstract Factory design pattern, Factory design pattern produces implementation of Products e.g. Garment Factory produce different kinds of clothes, On the other hand Abstract Factory design pattern adds another layer of abstraction over Factory Pattern and Abstract Factory implementation itself e.g. Abstract Factory will allow you to choose a particular Factory implementation based upon need which will then produce different kinds of products.

In short
1) Abstract Factory design pattern  creates Factory

2) Factory design pattern creates Products

e.g. Designing authentication system for a product, Authentication factory gives object for authentication of particular type based on input. e.g. for Windows Authentication it will give Identity Auth, for OWIN it will corresponding type, for forms-authentication, it will gave corresponding type. If we want to decouple whole system from underlying authentication, Abstract factory can give Interface of Authentication Factory that can be replace by any one of authentication system without impacting Outer system

AbstractFactory : Declares an interface for operations that create abstract product objects.

ConcreteFactory : Implements the operations declared in the AbstractFactory to create concrete product objects.

Product : Defines a product object to be created by the corresponding concrete factory and implements the AbstractProduct interface.

Client : Uses only interfaces declared by AbstractFactory and AbstractProduct classes.

