# Simple-Chatty-Bot
A simple personal assistant bot, created with the assistance of HyperSkill's lessons

The bot will ask your name, then guess your age, count to a given number, and test your programming knowledge.

package bot;

import java.util.Scanner;

public class SimpleBot {
    final static Scanner scanner = new Scanner(System.in);

    public static void main(String[] args) {
        greet("Optio", "2020");
        remindName();
        guessAge();
        count();
        test();
        end();
    }

    static void greet(String assistantName, String birthYear) {
        System.out.println("Hello! My name is " + assistantName + ".");
        System.out.println("I was created in " + birthYear + ".");
        System.out.println("Please, remind me your name.");
    }

    static void remindName() {
        String name = scanner.nextLine();
        System.out.println("What a great name you have, " + name + "!");
    }

    static void guessAge() {
        System.out.println("Let me guess your age.");
        System.out.println("Say me remainders of dividing your age by 3, 5 and 7.");
        int rem3 = scanner.nextInt();
        int rem5 = scanner.nextInt();
        int rem7 = scanner.nextInt();
        int age = (rem3 * 70 + rem5 * 21 + rem7 * 15) % 105;
        System.out.println("Your age is " + age + "; that's a good time to start programming!");
    }

    static void count() {
        System.out.println("Now I will prove to you that I can count to any number you want.");
        int num = scanner.nextInt();
        for (int i = 0; i <= num; i++) {
            System.out.printf("%d!\n", i);
        }
    }

    static void test() {
        while (true) {
            System.out.println("Let's test your programming knowledge.");
            System.out.println("What makes Java more versatile than other programming languages?");
            System.out.println("1. It can be written with any syntax.");
            System.out.println("2. It requires no programming knowledge.");
            System.out.println("3. It uses virtualization to run on many different operating Systems.");
            System.out.println("4. It can be written and run directly from the command prompt.");
            int ans = scanner.nextInt();
            if (ans == 3) {
                break;
            } else {
                System.out.println("Please, try again.");
            }
        }
    }

    static void end() {
        System.out.println("Congratulations, have a nice day!");
    }
}
