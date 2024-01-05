## Function overloading | Constructor Overloading

Two functions in the same class but having different signatures

#### Advantages

-   clean code
-   flexibility
-   easy to read
-   multiple return types
-   same name different behaviour
-   can have multiple constructures

## Function overridding

Override the function in the child class

#### Advantages

-   clean code
-   flexibility
-   easy to read
-   multiple return types based on classes
-   can have same function do different things in different classes

## Finialize Method

The Java finalize() method of Object class is a method that the Garbage Collector always calls just before the deletion/destroying the object which is eligible for Garbage Collection to perform clean-up activity

## Inheritance

-   Single-level inheritance
-   Multi-level inheritance
-   Hierarchical inheritance
-   Multiple inheritance
-   Hybrid inheritance

More info on: https://www.upgrad.com/blog/types-of-inheritance-in-java/

## Abstract vs interface

|                                        Abstract                                         |                                 Interface                                 |
| :-------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------: |
|                         Non Abstract method & Abstract Methods                          | Only Abstract methods, after java 8 finals and static methods are allowed |
|                           Multiple inheritance is not allowed                           |                      Multiple inheritance is allowed                      |
|                          final, non finals, static, non-static                          |                               final, static                               |
|                   Abstract class can have implementation of interface                   |                  interface cannot extend abstract class                   |
| An abstract class can extend another Java class and implement multiple Java interfaces. |           An interface can extend another Java interface only.            |
|                                    keyword: extends                                     |                            keyword: implements                            |
|       A Java abstract class can have class members like private, protected, etc.        |                          only public is allowed.                          |

## Exception

An exception is an unwanted event or unexpected event that occur during the execution of the program i.e. runtime, which disrupt the normal execution of the program. Exception can be caught and handled by the program. When an exception occurs, an object is created that object is called exception object and contains information about the exception such as the cause of the exception, name of the exception, description of the exception and state of the program.

#### Major reason of exception occurance

-   Invalid user input
-   Device failure
-   Loss of network connection
-   Physical limitations (out-of-disk memory)
-   Code errors
-   Opening an unavailable file

<b>Error</b>: An Error indicates a serious problem that a reasonable application should not try to catch.

<b>Exception</b>: Exception indicates conditions that a reasonable application might try to catch.

#### Exception types:

##### Checked exception

-   ClassNotFoundException
-   InstantiationException
-   InterruptedException
-   IOException
-   SQLException
-   FileNotFoundException

##### Unchecked exception

-   ArrayIndexOutOfBoundsException
-   ArithmeticException
-   NullPointerException
-   ClassCastException
-   ArrayStoreException
-   IllegalThreadStateException

## String Buffer Methods

-   append(string);
-   insert(start, string);
-   replace(start, end, string);
-   delete(start, end);
-   reverse()
-   capacity()

## String Methods

-   equals(string);
-   split(delimiter)
-   replace(kisko, kisse);
-   length()
-   toLowerCase()
-   toUpperCase()
-   charAt(int)
-   startsWith(string);
-   endsWith(string);

## Applet code to create Indian flag

```Java
import java.applet.Applet;
import java.awt.Color;
import java.awt.Graphics;

public class TricolorFlagApplet extends Applet {

    public void paint(Graphics g) {
        // Set background color as white
        setBackground(Color.white);

        // Dimensions of the flag
        int width = getSize().width;
        int height = getSize().height;

        // Calculate stripe height
        int stripeHeight = height / 3;

        // Draw Saffron (top) stripe
        g.setColor(Color.orange); // Saffron color
        g.fillRect(0, 0, width, stripeHeight);

        // Draw White (middle) stripe
        g.setColor(Color.white);
        g.fillRect(0, stripeHeight, width, stripeHeight);

        // Draw Green (bottom) stripe
        g.setColor(Color.green); // Green color
        g.fillRect(0, 2 * stripeHeight, width, stripeHeight);

        g.setColor(Color.black);
        g.drawOval(width / 2, height / 2, stripeHeight, stripeHeight);
    }
}

```
