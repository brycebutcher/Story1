
# Exam 2 review

This is a brief overview of what will be expected on the exam.

# Chapter 1, 2, 3, 4, and 5
## Make a:
* write a code that implements the bubble sort
```java
import java.util.Scanner;
public class Test2 {

	public static void main(String[] args) {
		// TODO Auto-generated method stub

		

		
		  
		    int num, i, j, temp;
		    Scanner input = new Scanner(System.in);
		 
		    System.out.println("Enter the number of integers to sort:");
		    num = input.nextInt();
		 
		    int array[] = new int[num];
		 
		    System.out.println("Enter " + num + " integers: ");
		 
		    for (i = 0; i < num; i++) 
		      array[i] = input.nextInt();
		 
		    for (i = 0; i < ( num - 1 ); i++) {
		      for (j = 0; j < num - i - 1; j++) {
		        if (array[j] > array[j+1]) 
		        {
		           temp = array[j];
		           array[j] = array[j+1];
		           array[j+1] = temp;
		        }
		      }
		    }
		 
		    System.out.println("Sorted list of integers:");
		 
		    for (i = 0; i < num; i++) 
		      System.out.println(array[i]);
		  }
		
	}
```	
* an if statement
```java
public class test {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		int sarah = 11;
		String emotion;		
		
		if (sarah<10) {
			emotion = "unhappy" ;
		} else {
			emotion = "happy";
		}
		
				
		System.out.println("Sarah feels " + emotion);
		
	}

}
```
* print statement
  ```java
	package test;

	public class test {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		System.out.println("This is my print statement.");
		
		}

	}

```

* int

```java
package test;

public class test {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		int wishMeLuck = 15;
				
		System.out.println(wishMeLuck);
```

* double
```java
package test;

public class test {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		double wishMeLuck = 15.5;
				
		System.out.println(wishMeLuck);
		
	}

}
```

* string
```java
package test;

public class test {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		String greeting = "Hello World";
				
		System.out.println(greeting);
		
	}

}
```

## Use



* for loop
```java
public class test {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		for (int x = 2; x<=5; x++)
		
				
		System.out.println("Value of x = " + x);
		
	}

}
```

* Math.random() to make a coin toss
```java
public class test {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		if (Math.random() < 0.5) System.out.println("Heads");
        else                     System.out.println("Tails");
	}

}
```

* Math.random() to make an integer between 1 and 1,000
```java
public class test { 
    public static void main(String[] args) {
        
       System.out.println(1 + Math.random() * 1000);
         
    }
}

```

* a trig function
```java
public class test { 
    public static void main(String[] args) {
        
       System.out.println(Math.sqrt(16));
         
    }
}
```

* a comparison of two strings
```java
public class test { 
    public static void main(String[] args) {
        
    	String s1 = "test";
        String s2 = "Test";
        
        System.out.println(s1.equals(s2));
        
     }
  }
```

* a comparison of two strings that ignores case
```java
public class test { 
    public static void main(String[] args) {
        
    	String s1 = "test";
        String s2 = "Test";
        
        System.out.println(s1.equalsIgnoreCase(s2));
        
     }
  }
  ```

* use a scanner
```java
import java.util.Scanner;

public class test { 
    public static void main(String[] args) {
        
    	Scanner input = new Scanner(System.in);
    	System.out.print("Enter either 1 or 2: ");
    	String hexString = input.nextLine();
    	
    	if (hexString.equals(1)) {
    		System.out.println("You are number 1 ");
    	}
    	else if(hexString.equals(2)) {
    		System.out.println("You are number 2 ");
    	}
    	else {
    		System.out.println("Whoops");
    	}
  }
    
}
```

# Chapter 6: Custom methods

I don't understand custom methods very well at all. I could really use some help on understanding these.
## make a custom method that:
* returns nothing (void) and accepts nothing();
```java
public class MyClass {
    public static void main(String args[]) {
        System.out.print("The grade is ");
        printGrade(78.5);
        
        System.out.print("The grade is ");
        printGrade(59.5);
        
    }
    public static void printGrade(double score) {
        if (score >= 90.0) {
            System.out.println('A');
        }
        else if (score >= 80.0) {
            System.out.println('B');
        }
        else if (score >= 70.0) {
            System.out.println('C');
        }
        else if (score >= 60.0) {
            System.out.println('D');
    
        }
        else {
            System.out.println('F');
        }
        }
    
}
```
* returns nothing and accepts an integer
Not sure if this is what you wanted, but I found this in the book.
```java
import java.util.Scanner;
public class Test2 {

	public static void main(String[] args) {
		// TODO Auto-generated method stub

	Scanner input = new Scanner(System.in);
		
	 // Prompt the user to enter two integers
	 System.out.print("Enter first integer: ");
	 int n1 = input.nextInt();
	 System.out.print("Enter second integer: ");
	 int n2 = input.nextInt();
		System.out.println("The greatest common divisor for " + n1 +
		  " and " + n2 + " is " + gcd(n1, n2));
			  }
				 
		  /** Return the gcd of two integers */
			  public static int gcd(int n1, int n2) {
			  int gcd = 1; // Initial gcd is 1
			  int k = 2; // Possible gcd
				 
			  while (k <= n1 && k <= n2) {
			  if (n1 % k == 0 && n2 % k == 0)
			 gcd = k; // Update gcd
			 k++;
		  }
				 
		  return gcd;
	}
		
	}
	```
* returns nothing and accepts a string
* returns an int and accepts nothing
```java
public class Test2 {

	//public static void main(String[] args) {
		// TODO Auto-generated method stub

		public static int sum(int i1, int i2) {
			int result = 0;
			 for (int i = i1; i <= i2; i++)
			 result += i;
			
			 return result;
			 }
			
			 public static void main(String[] args) {
			 System.out.println("Sum from 1 to 10 is " + sum(1, 10));
			 System.out.println("Sum from 20 to 37 is " + sum(20, 37));
			 System.out.println("Sum from 35 to 49 is " + sum(35, 49));
			 }
	}
```
* returns a double and accepts an int
* returns a string and accepts two ints
* returns a double and accepts an array
* returns an array and accepts an array

# Arrays
## Make a
* Single dimensional array
```java
	public class Array { 
	public static void main(String args[]) { 
	int month_days[]; 
   	  month_days = new int[12]; 
  	  month_days[0] = 31; 
  	  month_days[1] = 28; 
  	  month_days[2] = 31; 
  	  month_days[3] = 30; 
  	  month_days[4] = 31; 
  	  month_days[5] = 30; 
  	  month_days[6] = 31; 
  	  month_days[7] = 31; 
 	  month_days[8] = 30; 
  	  month_days[9] = 31; 
  	  month_days[10] = 30; 
  	  month_days[11] = 31; 
	System.out.println("April has " + month_days[3] + " days."); 
} 
}
```
* Multi dimensional array
```java
public class MultiArray{  
	public static void main(String args[]){  
  
	int a[]=new int[5];
	a[0]=10;
	a[1]=20;  
	a[2]=70;  
	a[3]=40;  
	a[4]=50;  
  
  
	for(int i=0;i<a.length;i++)
	System.out.println(a[i]);  
  
	}
}  
```
* Sort an array
```java
import java.util.Arrays;
 
public class SortExample
{
    public static void main(String[] args)
    {
        
        int[] arr = {13, 7, 6, 45, 21, 9, 101, 102};
 
        Arrays.sort(arr);
 
        System.out.printf("Sorted Array : %s",
                          Arrays.toString(arr));
    }
}
```
* Make a jagged array
```java
public class Test {

	public static void main(String[] args) {
		// TODO 
		int arr[][] = new int[2][];
		 
        
        arr[0] = new int[3];
       
        arr[1] = new int[2];
    
        int count = 0;
        for (int i=0; i<arr.length; i++)
            for(int j=0; j<arr[i].length; j++)
                arr[i][j] = count++;

        System.out.println("Jagged Array");
        for (int i=0; i<arr.length; i++)
        {
            for (int j=0; j<arr[i].length; j++)
                System.out.print(arr[i][j] + " ");
            System.out.println();
        }
    }

	}
```
