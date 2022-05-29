# Operator-Overloading

## Aim:
To write a C# program to find the volume of a box using operator overloading
 
## Algorithm:
1.Create a class for operator overloading

2.Get inputs for length,breadth and height of the box from the user and then calculate the volume in overloading function

3.After that return a new object for the calculated volume

4.Then create a new object to store the return object

5.After that print the calculated volume
 
## Program:
```c#
using System;
namespace Operator
{
    class Box
    {
        private double length;
        private double breadth;
        private double height;

        public double getVolume()
        {
            return length * breadth * height;
        }
        public void setLength(double l)
        {
            length = l;
        }
        public void setBreadth(double b)
        {
            breadth = b;
        }
        public void setHeight(double h)
        {
            height = h;
        }
        public static Box operator +(Box Box1, Box Box2)
        {
            Box box = new Box();
            box.length = Box1.length + Box2.length;
            box.breadth = Box1.breadth + Box2.breadth;
            box.height = Box1.height + Box2.height;
            return box;
        }
    }
    class Program
    {
        static void Main(string[] args)
        {
            Box Box1 = new Box();
            Box Box2 = new Box();
            Box Box3 = new Box();
            double volume = 0.0;

            Console.WriteLine("Box1:");
            Box1.setLength(Convert.ToDouble(Console.ReadLine()));
            Box1.setBreadth(Convert.ToDouble(Console.ReadLine()));
            Box1.setHeight(Convert.ToDouble(Console.ReadLine()));
            Console.WriteLine("Box2:");
            Box2.setLength(Convert.ToDouble(Console.ReadLine()));
            Box2.setBreadth(Convert.ToDouble(Console.ReadLine()));
            Box2.setHeight(Convert.ToDouble(Console.ReadLine()));
            
            volume = Box1.getVolume();
            Console.WriteLine("Volume of Box1 : {0}", volume);
            volume = Box2.getVolume();
            Console.WriteLine("Volume of Box2 : {0}", volume);
            Box3 = Box1 + Box2;
            Console.WriteLine("Volume of Box3: {0}", Box3.getVolume());
            Console.ReadKey();

        }
    }
}
 ```
## Output:
 
![img](https://user-images.githubusercontent.com/75413726/170867920-138a1f95-8729-4b59-aaa8-56d47118d48d.jpg)

## Result:

Thus the C# program to find the volume of a box using operator overloading was implemented.

