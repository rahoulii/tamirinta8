# tamirinta8


import java.util.Scanner;

public class tamirinta8 {

    public static void main(String[] args) {
        System.out.println("please inter your number!!!");
        Scanner s1 = new Scanner(System.in);
        int i = s1.nextInt();
        System.out.println("your answer swap is :" + swapDigitPairs(i));
        //System.out.println(7%10);
        int n = 75;
        n /= 10;
        System.out.println(n);
        

    }

    public static int swapDigitPairs(int number) {
        int result = 0;
        int place = 1;
        while (number > 9) {
            result += place * 10 * (number % 10);
            number /= 10;
            result += place * (number % 10);
            number /= 10;
            place *= 100;
        }
        return result + place * number;
    }
     
}
