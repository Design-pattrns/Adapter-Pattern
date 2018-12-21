# Adapter-Pattern
Adapter design pattern is one of the structural design pattern and it’s used so that two unrelated interfaces can work together. The object that joins these unrelated interface is called an Adapter. 


In normal development, the adapter (Adapter) is a very common mode, such as the Adapter of the commonly used RecyclerView, the Adapter of the ListView, and so on. But it is used frequently, but I don't know what the specific implementation principle of the adapter mode is. Then we will analyze this adapter mode with specific cases below.

First understand what an adapter is? The charger is usually used when charging the phone or charging the laptop. Because we know that the voltage on the board is 220 V, if it is directly connected to the device, it will burn out, then the role of the adapter is like this -- the two things that could not work together because of the interface mismatch Working together


## UML class diagram for Adapter Class/Object

It should be noted here that there are two types of adapters by type:
 + Class adapter
 + Object adapter

Below is the corresponding UML class diagram

> Class adapter

![](https://raw.githubusercontent.com/InnoFang/DesignPatterns/master/uml/class_adapter.png)

 + Target : Adapter interface
 + Adaptee :Role to be adapted
 + Adapter : Adapter that adapts the corresponding operations of the roles that need to be adapted

![](https://raw.githubusercontent.com/InnoFang/DesignPatterns/master/uml/object_adapter.png)

 The three characters here are the same, but the combination is used here.

So what is the difference between the two implementations here?
 + The same point: all APIs that convert the API of the adapted class to the target class.
 + difference：
   - Class adapters use inherited methods to connect to the Adaptee class
   - Object adapters connect to the Adaptee class in a combined way

The effect of using interface combination to achieve interface compatibility is more flexible. The advantage is that the methods in the adapted object are not exposed, and the class adapter can also use the method in the adapted object because it inherits the adapted object.

In contrast, using the object adapter pattern is more flexible and uses

## Simple implementation of adapter mode

In order to compare the two methods, the following two methods are implemented separately to charge the mobile device as an example, and convert the 220 V voltage into a 5 V voltage.




## to sum up

- advantage
  - Reusability: Better use of interfaces that do not meet system requirements by using adapters
  - Scalability: By using the adapter mode, you can extend your own functions in the original functions.
- Disadvantage
  - Excessive use of the adapter mode can make the system messy and difficult to grasp overall. Refactoring functions directly if not necessary

END.
