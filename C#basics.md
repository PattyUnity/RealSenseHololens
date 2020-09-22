# STARTING TO PROGRAM

## Floating Point Data types
Real numbers are represented by float and double. 
Real numbers are continuous but computer can only represents them in the discrete domain. 
Double has more bits than float.

When working with calculation, data type really matters. 
    int: int is for integer
    float: floating point numbers are approximations of the real numbers in the continuous domain
    double: double data types uses more bytes than the float data type and thus more accurate than float

## Type cast
ex1

    (float)Math.PI
ex2

    float cosine = (float)Math.Cos(degree * (float)Math.PI / 180);

## Prompting for and Getting
To prompt for an input, you could use something like:

    Console.Write("Enter first altitude: ");

To read, parse, and store an altitude typed in by the user, you could use something like:

    int firstAltitude=int.Parse(Console.ReadLine());
or    

    float angle = float.Parse(Console.ReadLine());
    
## Shorthand equation format
    // the line of code below is shorthand for
    // angle = angle * Math.PI / 180;
    angle *= (float)Math.PI / 180;
    
## Math Class Documentation
https://docs.microsoft.com/en-us/dotnet/api/system.math?view=netcore-3.1

## Runing the code multiple time with different inputs
```c#
        static void Main(string[] args)
        {
            // loop while there's more input
            string input = Console.ReadLine();
            while (input[0] != 'q')
            {
                // extract point coordinates from string
                GetInputValuesFromString(input);

                // Add your code between this comment
                // and the comment below. You can of
                // course add more space between the
                // comments as needed



                // Don't add or modify any code below
                // this comment
                input = Console.ReadLine();
            }    
        }

        /// <summary>
        /// Extracts point coordinates from the given input string
        /// </summary>
        /// <param name="input">input string</param>
        static void GetInputValuesFromString(string input)
        {
            // extract point 1 x
            int spaceIndex = input.IndexOf(' ');
            point1X = float.Parse(input.Substring(0, spaceIndex));

            // move along string and extract point 1 y
            input = input.Substring(spaceIndex + 1);
            spaceIndex = input.IndexOf(' ');
            point1Y = float.Parse(input.Substring(0, spaceIndex));

            // move along string and extract point 2 x
            input = input.Substring(spaceIndex + 1);
            spaceIndex = input.IndexOf(' ');
            point2X = float.Parse(input.Substring(0, spaceIndex));

            // point 2 y is the rest of the string
            input = input.Substring(spaceIndex + 1);
            point2Y = float.Parse(input);

            #region Unfortunately, Mono doesn't have a Split method!
            //string[] values = input.Split(' ');
            //point1X = float.Parse(values[0]);
            //point1Y = float.Parse(values[1]);
            //point2X = float.Parse(values[2]);
            //point2Y = float.Parse(values[3]);
            #endregion

        }    
```
# INTRODUCTION TO CLASSES AND OBJECTS

## The difference between classes and objects
### Class
* Template for creating objects
* Defines the fields, properties and behavior of every object of the class
* _Cookie cutter_
* Reference type
    
### Object
* Actual instance of the class in memory
* Each object stores its own state
    

## State, behavior, and identity of an object
### State 
* = Characteristics of the object
* Can change over time
* Stored in fields
* Accessed through __properties__
### Behavior
* = What we can do to the object
* = What the object to do to itself
* Accessed through __methods__
### Identity
* What we can distinguish one object from another
* Memory address of that object
* instantiate by __constructor__

Fields, properties and methods are represented in UML which stands for **Unified Modeling Language**

## How to use constructor
* To create or instantiate an object and give __identity__ to the object
* Require a ()

## How to use properties
* To access __state__ of and object
* Does not require a parentheses ()

## How to use methods
* To access __behaviours__ of an object
* Require a () 

