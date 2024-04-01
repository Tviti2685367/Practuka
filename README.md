import java.util.Scanner;

public class Calculator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        double num1, num2;
        char operator;
        
        System.out.print("Введіть перше число: ");
        num1 = scanner.nextDouble();
        System.out.print("Введіть друге число: ");
        num2 = scanner.nextDouble();
        System.out.print("Введіть операцію (+, -, *, /): ");
        operator = scanner.next().charAt(0);
        
        double result;
        switch(operator) {
            case '+':
                result = num1 + num2;
                break;
            case '-':
                result = num1 - num2;
                break;
            case '*':
                result = num1 * num2;
                break;
            case '/':
                if(num2 != 0)
                    result = num1 / num2;
                else {
                    System.out.println("Помилка: ділення на нуль");
                    return;
                }
                break;
            default:
                System.out.println("Невідома операція");
                return;
        }
        
        System.out.println("Результат: " + result);
    }
}



