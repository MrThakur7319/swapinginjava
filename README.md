# swapinginjava
// Import Scanner class for taking user input
import java.util.Scanner;

// Main class for demonstrating variable swapping techniques
public class Swapvarible{
 public static void main(String[] args){
   // Create a Scanner object to read input from the console
   Scanner sc = new Scanner(System.in);
   
   // Get the first number from user
   System.out.println("enter the value of a");
   int a = sc.nextInt();
   
   // Get the second number from user
   System.out.println("enter the value of b");
   int b = sc.nextInt();
   
   // Display the original values before swapping
   System.out.println("a: " + a + " b: " + b);
   System.out.println("type two of swapping ");
   
   // ===== METHOD 1: SWAPPING USING TEMPORARY VARIABLE =====
   // Copy original values to new variables for first swapping method
   int x = a;
   int y = b;
   
   // Use a temporary variable to swap values
   int temp = x;  // Store x in temporary variable
   x = y;         // Assign y's value to x
   y = temp;      // Assign temp (original x value) to y

   // Display results of first swapping method
   System.out.println("a = " + x + " b = " + y);

   // ===== METHOD 2: SWAPPING WITHOUT TEMPORARY VARIABLE =====
   // Copy original values to new variables for second swapping method
   int p = a;
   int q = b;
   
   // Mathematical approach to swap without using extra memory
   p = p + q;     // p now contains sum of both numbers
   q = p - q;     // q = (p + q) - q = p (original value of p)
   p = p - q;     // p = (p + q) - p = q (original value of q)
   
   // Display results of second swapping method
   System.out.println("a = " + p + " b = " + q);
   
   // Program completion message
   System.out.println("program ended successfully");

   // Close the Scanner to free up system resources
   sc.close();
 }
}
