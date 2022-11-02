# desen-gore-recursive
import java.util.Scanner;

public class Main {

    static int negative(int x) {
        if (x <= 0) {
            return x;
        } else {
            System.out.print(x + " ");
            return negative(x - 5);
        }
    }

    static int positive(int x, int y) {
        if (x > y) {
            return x;
        } else {
            System.out.print(x + "");
            return positive(x + 5, y);
        }
    }


    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        while (true) {
            System.out.print("Bir sayi giriniz: ");
            int sayi = input.nextInt();

            positive(negative(sayi), sayi);

            if (sayi == 0) {
                break;
            }
            System.out.println( "\nçıkmak için 0'ı tuşlayınız." );
        }
    }
}
































