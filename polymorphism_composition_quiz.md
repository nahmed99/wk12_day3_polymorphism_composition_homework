# Polymorphism & Composition Homework - Quiz

# Polymorphism

1. What does the ___word___ 'polymorphism' mean?

Many forms (or shapes).


2. What does it mean when we apply polymorphism to OO design? Give a simple Java example.

A class can have sub-classes (that extend it), inheriting its properties and behaviours. 
For example, a Life class could have sub-classes Animal and Plant. These would inherit 
properties (e.g., mass, height, colour) and behaviours (e.g., grow(), respire(), consume() etc)
from the Life class. The sub-classes have a 'is-a' relationship with the super-class;
they are different forms of the Life class.

class Life{}
class Plant extends Life {}
class Animal extends Life {}


Another example would be overloading of methods; multiple methods that have the same name 
but different arguments. For example, the consume() class above could have one argument 
passed to it for (some) plants, 'water', and for animals it could have two arguments, food 
and water.

public void consume(String water) {}
public void consume(String water, String food) {}



3. What can we use to implement polymorphism in Java?

The 'extends' keyword in the case of classes. We could also use the word 'implements'
when inheriting from interfaces in classes.


4. How many 'forms' can an object take when using polymorphism?

A class can only entend one other class, but can implement multiple interfaces.


5. Give an example of when you could use polymorphism.

Please refer to answer for question 2; Life class and consume() method examples.



# Composition

6. What do we mean by 'composition' in reference to object-oriented programming?

When something (an object) is composed of other objects.


7. When would you use composition? Provide a simple example in Java.

Is this referring to dependency inversion (DI)? You would use DI when you want
to ensure that a higher-order class is not dependent upon a lower class. Rather
than create new instances in the higher-order class, accept instances of the lower
order as parameters into the class. 

Please read "object" where they are instances of the class.

Use the following

class Car {

    private Engine engine;
    private SuctionControlValve scv;

    public Car (Engine engine, SuctionControlValve scv) {
        this.engine = engine;
        this.scv = scv;
    }

}

instead of:

class Car {

    private Engine engine;
    private SuctionControlValve scv;

    public Car (Engine engine, SuctionControlValve scv) {
        engine = new Engine(~ ~ ~ );
        scv = new SuctionControlValve(~ ~ ~);
    }

}


8. What is/are the advantage(s) of using composition?

The higher order class (object) is NOT dependent upon the lower order class (object).


9. When an object is destroyed, what happens to all the objects it is composed of?

All objects that it is composed of are also destroyed.