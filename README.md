# Sale-Application-System
import java.util.Scanner;

public class YourName {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        // Declare variables for products
        double price1, price2, price3;
        int qty1, qty2, qty3;
        double totalAmount, discountRate, totalDiscount, amountDue, amountTendered, change;

        // Input for Product #1
        System.out.print("Enter Price for Product #1: ");
        price1 = input.nextDouble();
        System.out.print("Enter Quantity for Product #1: ");
        qty1 = input.nextInt();

        // Input for Product #2
        System.out.print("Enter Price for Product #2: ");
        price2 = input.nextDouble();
        System.out.print("Enter Quantity for Product #2: ");
        qty2 = input.nextInt();

        // Input for Product #3
        System.out.print("Enter Price for Product #3: ");
        price3 = input.nextDouble();
        System.out.print("Enter Quantity for Product #3: ");
        qty3 = input.nextInt();

        // Calculate total amount
        totalAmount = (price1 * qty1) + (price2 * qty2) + (price3 * qty3);
        System.out.println("Total Amount: " + totalAmount);

        // Input for discount rate
        System.out.print("Enter Discount Rate (%): ");
        discountRate = input.nextDouble();

        // Calculate discount and amount due
        totalDiscount = (discountRate / 100) * totalAmount;
        amountDue = totalAmount - totalDiscount;
        System.out.println("Total Discount: " + totalDiscount);
        System.out.println("Amount Due (less discount): " + amountDue);

        // Input for amount tendered
        System.out.print("Enter Amount Tendered: ");
        amountTendered = input.nextDouble();

        // Calculate change
        change = amountTendered - amountDue;
        System.out.println("YOUR CHANGE IS: " + change);

        input.close();
    }
}
