# Operator-Overloading

## Aim:
 To write a C# program to pass values through constructors(default and parameterized) and also overload equal operators by checking whether objects are equal using operator overloading. 
 
## Algorithm: 
### Step 1:
Create a class operator

### Step 2:
Pass values through the constructor

### Step 3:
return the bool operator, (==) and (!=)

### Step 4:
create a object to store the return object

### Step 5:
print the program.
 
## Program:
~~~
using System;
class overload
{
  public int num1, num2;
  public overload()
  {
      num1 = 20;
      num2 = 20;
      Console.WriteLine("this is a default constructor \n the value is " + this.num1);
      Console.WriteLine("this is a default constructor \n the value is " + this.num2);

  }
  public overload(int num1, int num2)
  {
      this.num1 = num1;
      this.num2 = num2;
      Console.WriteLine("this is a parameterized constructor");
      Console.WriteLine("the value is " + this.num1);
      Console.WriteLine("the value is " + this.num2);
  }
  
  public static bool operator==(overload ex1,overload ex2)
  {
         
      return ex1.Equals(ex2);
  }
  public static bool operator !=(overload ex1, overload ex2)
  {
      return !ex1.Equals(ex2);    
  }


public static void Main()
  {
      overload ex1 = new overload();
      overload ex2 = new overload(20,20);
      overload ex3 = ex2;
      if (ex1 == ex2)
      {
          Console.WriteLine("both the object are equal");
      }
      else if(ex1!=ex2)
      {
          Console.WriteLine("both are differtnt");
      }


  }

}
~~~

## Output:
![img 1](https://user-images.githubusercontent.com/94174536/236783028-f614bb9c-91c5-4146-9747-fc4b815121d3.png)
 
## Result:
Thus the C# program to find the volume of a box using operator overloading is implemented successfully.

