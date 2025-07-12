package codsoftProject;
import java.util.Random;
import java.util.Scanner;

public class Numbergame {
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        Random r=new Random();
        boolean play=true;
        while(play) {
            int rnumber= r.nextInt(100)+1;
            int guess;
            int attempt =0;
            int maxAttempt=10;
            System.out.println("welcome you to game ! best wishes ");
            System.out.println("plz guess any number between 1 to 100 . you have 10 chance");
            while(true) {
                System.out.println("enter your guess number :");
                guess = sc.nextInt();
                attempt++;
                if (guess == rnumber) {
                    System.out.println("congrates you guess" + attempt + "attempt");
                    break;
                } else if (guess > rnumber) {
                    System.out.println("high");
                } else {
                    System.out.println("low");
                }
                if (attempt == maxAttempt) {
                    System.out.println("your limit is over and the number was :" + rnumber);
                    break;
                }
            }
            System.out.println("want to play again (yes/no):");
            String response= sc.next();
            play=response.equalsIgnoreCase("yes");
                }
            System.out.println("Thank you for playing :");
             sc.close();
            }
        }

