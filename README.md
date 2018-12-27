# Everest
import java.util.Scanner;

public class P04_Everest {
    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);

        String willNightOver = scanner.nextLine();
        int metersHigh = 5364;
        int couter = 1;
        int mountEverest = 8848;

        while (!willNightOver.equalsIgnoreCase("end")){

            if (willNightOver.equalsIgnoreCase("yes")){
                couter++;
            }

            if (couter > 5){
                break;
            }

            int metersLifted = Integer.parseInt(scanner.nextLine());

            metersHigh = metersHigh + metersLifted;

            if (metersHigh >= mountEverest){
                break;
            }


            willNightOver = scanner.nextLine();
        }

        if (metersHigh >= mountEverest){
            System.out.printf("Goal reached for %d days!",couter);
        }
        else {
            System.out.printf("Failed!\n%d", metersHigh);
        }
    }

}
