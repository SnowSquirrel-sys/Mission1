# Mission1
import java.util.Scanner;

public class Hello {
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);

       System.out.println("Hello! Good to see you!");
       int Size, tmp = 0, Check1 = 0, Check2 = 0;
        Size = in.nextInt();
       while (Size < 0 || Size >= 10) {
           System.out.println("ERROR");
           System.out.println("Enter The Numbers Again Please");
           Size = in.nextInt();
       }
        System.out.println("Now 'Cin' (lol) the numbers");
       int[] Vec1 = new int[10];
       for (int i = 0; i < 10; i++) {
           Vec1[i] = i;
           Vec1[i] = in.nextInt();
           if (i == Size) {
               tmp = Vec1[i];
               Check2 = 1;
           }
           if (Vec1[i] <= 0) {
               System.out.println("ERROR");
               Check1 = 1;
           }

       }
       if (tmp != 0 &&  Check1 != 1) {
           System.out.println("The Number Found, And The List Is Correct");
           System.out.println(tmp);
           Check1 = 2;
       }
       if (tmp != 0 && Check1 != 2) {
           System.out.println("The Number Found, But The List Is UnCorrected");
           System.out.println(tmp);

       }
       if (tmp == 0 && Check1 != 1){
           System.out.println("The Number Didn't Found, But The List Is Correct");
           System.out.println(tmp);
           Check2 = 0;
        }
       if (tmp == 0 && Check2 != 0){
           System.out.println("The Number Didn't Found, And The List Is UnCorrected");
           System.out.println(tmp);
       }

    }
}
