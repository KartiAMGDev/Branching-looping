# Branching-looping
1) Write a program to print the numbers from 10 to 50 using for loop/while loop.

public class PrintNumbers {
    public static void main(String[] args) {
        // Print numbers from 10 to 50 using a for loop
        System.out.println("Numbers from 10 to 50:");
        for (int i = 10; i <= 50; i++) {
            System.out.println(i);
        }
    }
}

public class PrintNumbers {
    public static void main(String[] args) {
        // Print numbers from 10 to 50 using a while loop
        System.out.println("Numbers from 10 to 50:");
        
        int number = 10; // Starting number
        
        while (number <= 50) {
            System.out.println(number);
            number++;
        }
    }
}

2) Write a program that find a given number is negative or positive

import java.util.Scanner;

public class CheckNumber {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Get user input for the number
        System.out.print("Enter a number: ");
        int number = scanner.nextInt();

        // Check if the number is negative, positive, or zero
        if (number < 0) {
            System.out.println("The entered number is negative.");
        } else if (number > 0) {
            System.out.println("The entered number is positive.");
        } else {
            System.out.println("The entered number is zero.");
        }

        
        scanner.close();
    }
}

3) Write down the program to reverse the given number using loops.
Input = 876 Output=678

public class ReverseNumber {
    public static void main(String[] args) {
        int number = 876;

        // Reverse the number using a while loop
        int reversedNumber = 0;
        while (number != 0) {
            int digit = number % 10;
            reversedNumber = reversedNumber * 10 + digit;
            number = number / 10;
        }

        System.out.println("Reversed number: " + reversedNumber);
    }
}


4) Write a java program to Find the smallest number among three numbers.

import java.util.Scanner;

public class SmallestNumber {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Get user input for three numbers
        System.out.print("Enter the first number: ");
        int num1 = scanner.nextInt();

        System.out.print("Enter the second number: ");
        int num2 = scanner.nextInt();

        System.out.print("Enter the third number: ");
        int num3 = scanner.nextInt();

        // Find the smallest number using nested if statements
        int smallestNumber = num1;

        if (num2 < smallestNumber) {
            smallestNumber = num2;
        }

        if (num3 < smallestNumber) {
            smallestNumber = num3;
        }

        System.out.println("The smallest number among " + num1 + ", " + num2 + ", and " + num3 + " is: " + smallestNumber);

        
        scanner.close();
    }
}

5. Write a Java program that takes the purchase amount as input and calculates the final payable amount after applying the discount.
1. If the purchase amount is less than 500, no discount is applied.
2. If the purchase amount is between 500 and 1000, a 10% discount is applied.
3. If the purchase amount is greater than 1000 a 20% discount is applied.

import java.util.Scanner;

public class PurchaseDiscount {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Get user input for the purchase amount
        System.out.print("Enter the purchase amount: ");
        double purchaseAmount = scanner.nextDouble();

        // Calculate the discount and final payable amount
        double discount = 0.0;
        double finalAmount = 0.0;

        if (purchaseAmount < 500) {
            // No discount for purchases less than 500
            finalAmount = purchaseAmount;
        } else if (purchaseAmount <= 1000) {
            // 10% discount for purchases between 500 and 1000
            discount = 0.1 * purchaseAmount;
            finalAmount = purchaseAmount - discount;
        } else {
            // 20% discount for purchases greater than 1000
            discount = 0.2 * purchaseAmount;
            finalAmount = purchaseAmount - discount;
        }

        // Display the results
        System.out.println("Purchase Amount: $" + purchaseAmount);
        System.out.println("Discount Applied: $" + discount);
        System.out.println("Final Payable Amount: $" + finalAmount);

        
        scanner.close();
    }
}


6..Write a java program to print below pattern
55555
54444
54333
54322
54321

import java.util.Scanner;

public class PatternPrint {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Enter the number of rows:");
        int k = scanner.nextInt();

        for (int i = k; i >= 1; i--) {
            for (int j = k; j >= 1; j--) {
                System.out.print(i > j ? i : j);
            }
            System.out.println();
        }

       
        scanner.close();
    }
}
