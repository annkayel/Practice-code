import java.util.Scanner;

public class DaysInMonth {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        // Step 1: Get user input
        System.out.print("Enter a year: ");
        int year = input.nextInt();

        System.out.print("Enter a month (1-12): ");
        int month = input.nextInt();

        int days;

        // Step 2: Calculate number of days
        switch (month) {
            case 1: case 3: case 5: case 7: case 8: case 10: case 12:
                days = 31;
                break;
            case 4: case 6: case 9: case 11:
                days = 30;
                break;
            case 2:
                // Leap year check
                if ((year % 400 == 0) || (year % 4 == 0 && year % 100 != 0)) {
                    days = 29;
                } else {
                    days = 28;
                }
                break;
            default:
                System.out.println("Invalid month entered.");
                return;
        }

        // Step 3: Display output
        System.out.println(days + " days");
    }
}# Practice-code