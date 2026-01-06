# first-program

import java.util.Scanner;

public class PrimesFrom1ToN {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter N: ");
        int n = sc.nextInt();

        System.out.println("Prime numbers from 1 to " + n + " are:");
        for (int number = 2; number <= n; number++) {
            if (isPrime(number)) {
                System.out.print(number + " ");
            }
        }
        sc.close();
    }

    static boolean isPrime(int num) {
        if (num <= 1) return false;
        for (int i = 2; i <= num / 2; i++) {
            if (num % i == 0) return false;
        }
        return true;
    }
}
