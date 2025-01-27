# Interface

package calculatorprogram;
import java.util.Scanner;
interface Calculator{
    double add(double a,double b);
    double subtract(double a,double b);
    double multiply(double a,double b);
    double divide(double a,double b);
}
class SimpleCalculator implements Calculator {
public double add(double a, double b) {
return a + b;
}
public double subtract(double a, double b) {
return a - b;
}
public double multiply(double a, double b) {
return a * b;
}
public double divide(double a, double b) {
    if(b==0){
        System.out.println("Error:Division by Zero is Not Allowed!");
        return Double.NaN;
    }
return a / b;
}
}
    public static void main(String[] args) {
        Scanner scanner=new Scanner(System.in);
        Calculator calculator=new SimpleCalculator();
        System.out.println("Welcome to The Simple Calculator!!");
        System.out.print("enter the first number:");
        double num1=scanner.nextDouble();
        System.out.print("Enter the Second Number:");
        double num2=scanner.nextDouble();
        System.out.println("\n Result:");
        System.out.println("Addition:"+calculator.add(num1,num2));
        System.out.println("Subtraction:"+calculator.subtract(num1,num2));
        System.out.println("Multiplication:"+calculator.multiply(num1,num2));
        System.out.println("Division:"+calculator.divide(num1,num2));
        scanner.close();
    }
}

Output:
Welcome to The Simple Calculator!!
enter the first number:10
Enter the Second Number:5

 Result:
Addition:15.0
Subtraction:5.0
Multiplication:50.0
Division:2.0


