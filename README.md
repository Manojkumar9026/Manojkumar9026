import java.util.Scanner;

public class TextAdventureGame {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Welcome to the Adventure Game!");
        System.out.println("Choose a path: A or B");

        String userChoice = scanner.nextLine();

        if (userChoice.equalsIgnoreCase("A")) {
            System.out.println("You chose path A. Now, choose 1 or 2");
            userChoice = scanner.nextLine();

            if (userChoice.equals("1")) {
                System.out.println("You found a treasure! You win!");
            } else if (userChoice.equals("2")) {
                System.out.println("Oops! You fell into a trap. Game over!");
            } else {
                System.out.println("Invalid input. Game over!");
            }

        } else if (userChoice.equalsIgnoreCase("B")) {
            System.out.println("You chose path B. Now, choose X or Y");
            userChoice = scanner.nextLine();

            if (userChoice.equalsIgnoreCase("X")) {
                System.out.println("You encountered a friendly creature. You win!");
            } else if (userChoice.equalsIgnoreCase("Y")) {
                System.out.println("Uh-oh! You encountered a monster. Game over!");
            } else {
                System.out.println("Invalid input. Game over!");
            }

        } else {
            System.out.println("Invalid input. Game over!");
        }

        scanner.close();
    }
}
