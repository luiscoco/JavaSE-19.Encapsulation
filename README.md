# JavaSE-19.Encapsulation

See the Udemy course: https://www.udemy.com/course/curso-certificacion-profesional-desarrollador-java-se-11

It refers to the bundling of data (attributes) and methods (functions) that operate on the data into a single unit, often called a class.

The idea is to hide the internal implementation details of an object and only expose what is necessary.

Here's a simple example to illustrate encapsulation in Java:

```java
public class Person {
    // private fields (attributes)
    private String name;
    private int age;

    // public methods to access and modify the private fields
    public String getName() {
        return name;
    }

    public void setName(String newName) {
        // Perform validation or other logic before setting the name
        name = newName;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int newAge) {
        // Perform validation or other logic before setting the age
        if (newAge > 0) {
            age = newAge;
        } else {
            System.out.println("Invalid age");
        }
    }
}

public class Main {
    public static void main(String[] args) {
        // Creating an instance of the Person class
        Person person = new Person();

        // Accessing and modifying the private fields through public methods
        person.setName("John");
        person.setAge(25);

        // Retrieving and printing the information
        System.out.println("Name: " + person.getName());
        System.out.println("Age: " + person.getAge());
    }
}
```

In this example:

The Person class has private fields (name and age) to store information.

Public methods (getName, setName, getAge, and setAge) are provided to access and modify the private fields.

The encapsulation ensures that the internal state of the Person object is controlled and validated through these methods.

By encapsulating the data and providing controlled access, you can manage the object's state more effectively, enforce validation rules, and make changes to the internal implementation without affecting the external code that uses the class.
