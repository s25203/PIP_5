# PIP_5
import org.w3c.dom.ls.LSOutput;

import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        //z1();
        //System.out.println(z2(7));
        //z3(7);
        z4(5,3,8);
    }

    static void z4(int x0, int x1, int x2) {
        int max;

        if(x0 >= x1 && x0 >= x2) max = x0;
        else if(x1 >= x0 && x1 >= x2) max = x1;
        else max = x2;

            for(int i = max; i > 0; i--) {
                System.out.print(i + "\t");
                for (int j = 0; j < 3; j++) {
                    switch (j) {
                        case 0: {
                            System.out.print( i <= x0 ? "*" : " ");;
                        } break;
                        case 1: {
                            System.out.print( i <= x1 ? "*" : " ");;
                        } break;
                        case 2: {
                            System.out.println( i <= x2 ? "*" : " ");;
                        } break;
                    }
                }
            }
    }
    static void z3(int input) {
        if(input % 2 == 0) input--;

        int rowCount = (input / 2) + 1;
        int starCount = 1;
        int whitespaceCount = input / 2;

        for(int i = 0; i < rowCount; i++) {
            for (int j = 0; j < whitespaceCount; j++) {
                System.out.print(" ");
            }

            for(int k = 0; k < starCount; k++) {
                System.out.print("*");
            }

            for (int j = 0; j < whitespaceCount; j++) {
                System.out.print(" ");
            }

            starCount += 2;
            whitespaceCount--;

            System.out.println();
        }
    }

    static int z2(int input){
        if( input == 0 || input == 1 ) return 0;
        else if ( input == 2) return 1;
        return z2(input - 1) + z2(input - 2);
    }






    static void z1() {
        System.out.println("enter number");
        Scanner in = new Scanner(System.in);

        int input = Integer.parseInt(in.nextLine());

        showN(input);
    }

    static void showN(int input) {
        if (input > 0) {
            for (int i = 0; i <= input; i++) {
                System.out.print(i + "\t");
            }
        }
        if(input < 0) {
            for (int i = 0; i >= input; i--) {
                System.out.print(i + "\t");
            }
        }

        if (input == 0) System.out.print("0");
    }

}
