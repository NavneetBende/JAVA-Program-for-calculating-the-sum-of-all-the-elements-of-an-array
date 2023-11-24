# JAVA-Program-for-calculating-the-sum-of-all-the-elements-of-an-array

Sum of all the elements of an array
 

In this section, we learn about Program for calculating the sum of all the elements of an array in java programming language. We are given with an array and need to find the sum of the given elements of the array. We will discuss various approaches to find the solution of the given problem.


Here, we will discuss different methods to find the required sum of the elements of the array. Different methods discussed on this page are :

Method 1 : Using Iteration
Method 2 : Using recursion (Top-Down Approach)
Method 3 : Using recursion (Bottom-up Approach)
Method 1 :
Create a variable say sum = 0.
Run a loop to iterate over the entire array.
Set sum = sum + arr[i]
After complete iteration print(sum)
Method 1 : Java Code
Run
import java.util.Scanner;

public class Main
{
   public static void main(String args[])
   {

       int arr[] = {12, 13, 1, 10, 34, 10};

       int sum = 0;

       for(int i=0; i<arr.length; i++)
       {
         sum = sum + arr[i];
       }

       System.out.print(sum); 
   }
}
Output :
80
Related Pages
Find the Smallest and largest element in an array

Find Second Smallest Element in an Array

Reverse an Array

Sort first half in ascending order and second half in descending 

Sort the elements of an array

Method 2 :
Declare a recursive function say getSum(int arr[], int index, int len)
If(index==len-1) return arr[index]
Otherwise, return (arr[index] + getSum(arr, index+1, len))
Method 2 : Java Code
Run
import java.util.Scanner;

public class Main
{
   static int getSum(int arr[], int index, int len){

       if(index==len-1)
         return arr[index];

       return arr[index] + getSum(arr, index+1, len);
   }
   public static void main(String args[])
   {

      int arr[] = {12, 13, 1, 10, 34, 10};

      int n = arr.length;
      System.out.print(getSum(arr, 0, n)); 
   }
}
Output :
80
Method 3 :
Create a recursive function say getSum(int arr[], int index)
If(index==0) return arr[index]
Otherwise, return (arr[index] + getSum(arr, index-1))
Method 3 : Java Code
Run
import java.util.Scanner;

public class Main
{
   static int getSum(int[] arr, int index){

       if(index==0)
         return arr[index];

       return arr[index] + getSum(arr, index-1);
   }
   public static void main(String args[])
   {

      int arr[] = {12, 13, 1, 10, 34, 10};

      int n = arr.length;
      System.out.print(getSum(arr, n-1)); 
   }
}
Output :
80
