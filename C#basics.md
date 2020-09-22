

# Floating Point Data types
Real numbers are represented by float and double. 
Real numbers are continuous but computer can only represents them in the discrete domain. 
Double has more bits than float.

When working with calculation, data type really matters. 
    int: int is for integer
    float: floating point numbers are approximations of the real numbers in the continuous domain
    double: double data types uses more bytes than the float data type and thus more accurate than float

# Type cast
ex1

    (float)Math.PI
ex2

    float cosine = (float)Math.Cos(degree * (float)Math.PI / 180);

# Prompting for and Getting
To prompt for an input, you could use something like:

    Console.Write("Enter first altitude: ");

To read, parse, and store an altitude typed in by the user, you could use something like:

    int firstAltitude=int.Parse(Console.ReadLine());
or    

    float angle = float.Parse(Console.ReadLine());
    
# Shorthand equation format
    // the line of code below is shorthand for
    // angle = angle * Math.PI / 180;
    angle *= (float)Math.PI / 180;
    
# Math Class Documentation
https://docs.microsoft.com/en-us/dotnet/api/system.math?view=netcore-3.1

# Runing the code multiple time with different inputs
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
    

