# Introduction

## Inheritance

Inheritance is a core concept in Object-Oriented Programming (OOP). It represents an IS-A relationship, also known as a parent-child relationship. In this relationship, a child inherits properties from the parent, much like the concept of inheritance in everyday English. In Java, these properties refer to fields and methods.

Consider a class, `Animal`:

```java
//Creating an Animal class with speak() as a member function.
public class Animal {

    public void speak() {
        System.out.println("This is an animal");
    }

}
```

We can then create a `Lion` class with the `Animal` class as a parent using the `extends` keyword:

```java
//Lion class is a child class of Animal.
public class Lion extends Animal {

    @Override
    public void speak() {
        System.out.println("Lion here!!");
    }

}
```

Because `Lion` is a child class of `Animal`, it inherits the fields and methods from its parent.

~~~~exercism/note
The `Override` annotation is used to indicate that a method in a subclass is overriding a method of its superclass.
It's not strictly necessary but it's a best practice to use it.
~~~~

Now whenever we do,

```java
Animal animal = new Lion(); //creating instance of Animal, of type Lion
animal.speak();
```

Note: Initialising the `Animal` class with `Lion`.
The output will look like

```java
Lion here!!
```

There are many types of inheritance, but Java only supports some of them (single, multi-level and hierarchical). To learn more about inheritance, please read [this][java-inheritance].

[java-inheritance]: https://www.javatpoint.com/inheritance-in-java
