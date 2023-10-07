import java.util.Scanner;

public class Calculator{
    public static void main(String[] args){

        //Starting scanner
        Scanner scanner = new Scanner (System.in);

        System.out.println("Simple Calculator");
        System.out.println("Available operations:");
        System.out.println("1. Addition (+)");
        System.out.println("2. Subtraction (-)");
        System.out.println("3. Multiplication (*)");
        System.out.println("4. Division (/)");

        System.out.print("Enter the operation number: ");
        int operation = scanner.nextInt();

        System.out.print("Enter the first number: ");
        double num1 = scanner.nextDouble();

        System.out.print("Enter the second number: ");
        double num2 = scanner.nextDouble();

        double result = 0.0;

        switch (operation) {
            case 1:
                result = num1 + num2;
                break;

            case 2:
                result = num1 - num2;
                break;

            case 3:
                result = num1 * num2;
                break;

            case 4:
                if (num2 != 0) {
                    result = num1 / num2;
                } 
                
                else {
                    System.out.println("Error: Division by zero is not allowed.");
                    System.exit(1);
                }
                break;

            default:
                System.out.println("Invalid operation.");
                System.exit(1);
        }

        System.out.println("Result: " + result);

        scanner.close();

     }

}
