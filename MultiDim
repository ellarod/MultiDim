11/1/2023
CSE 7 Fall 23: Classwork: Overloading Methods w/ Multidimensional Arrays	  
In this activity, you will practice defining and invoking overloaded methods to randomly fill and calculate the averages of multidimensional arrays.     
VSCode / JDK 11
*/

import java.util.Scanner;
import java.util.Arrays;
public class MultiDimAverage {

    public static void fillArray(double[][] arr1) {
        for(int r = 0; r< arr1.length; r++){
            for(int c= 0; c< arr1[r].length; c++){
                arr1[r][c] = (Math.random() * 100 + 1);
            }
        }
    }

    public static void fillArray(int[][] arr1) {
        for(int r = 0; r< arr1.length; r++){
            for(int c= 0; c< arr1[r].length; c++){
                arr1[r][c] = (int)(Math.random() * 100 + 1);
            }
        }
        
    }

    public static double findAverage(int[][] list) {
       double sum = 0;
       int elements = 0; //if you know that each row has the smae length, can use list.length*list

       for(int r = 0; r < list.length; r++){
        for(int c = 0; c < list[r].length; c++){
            sum += list[r][c];
            elements++;    
        }
       } 
       return sum/elements;
    }
    
    public static double findAverage(double[][] list) {
       double sum = 0;
       int elements = 0; //if you know that each row has the smae length, can use list.length*list

       for(int r = 0; r < list.length; r++){
        for(int c = 0; c < list[r].length; c++){
            sum += list[r][c];
            elements++;    
        }
       } 
       return sum/elements;
        
    }
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        System.out.println("Enter the number of Rows");
        int rows = getLength(s);
        System.out.println("Enter the number of Cols");
        int cols = getLength(s);
        System.out.println("Enter the type of array");
        char type = getType(s);

        switch (type) {
            case 'i':
                //todo: create a 2D integer array of size rowxcol

                int [][] arrI = new int [rows][cols];

                fillArray(arrI);
                System.out.println(Arrays.toString(arrI));//prints memory addresses of each array element arrI[0], arrI[1], ...
                System.out.println(Arrays.deepToString(arrI)); //prints the individual integer values instead
                System.out.println("The average of the above matrix is: " + findAverage(arrI));
                break;

            case 'd':
                //todo: create a 2D double array of size rowxcol
                double[][] arrD = new double[rows][cols];

                fillArray(arrD);
                System.out.println(Arrays.toString(arrD)); //prints memory addresses of each array element
                System.out.println(Arrays.deepToString(arrD)); //prints the individual double values instead
                System.out.println("The average of the above matrix is: " + findAverage(arrD));
                break;
        }

        s.close();
    }
    public static char getType(Scanner scan){
        char type = '\u0000';
        boolean loopControl = true;
        do{
            System.out.println("enter an i or d");
            type = scan.nextLine().charAt(0);
            if(type == 'i' || type == 'd'){
                loopControl = false;
            } else {
                System.out.println("invalid type, try again");
            }
        }while(loopControl);
        return type;
    }
    public static int getLength(Scanner scan){
        int length = 0;
        boolean loopControl = true;
        do{
            System.out.println("Enter a number between 2 and 25");
            if(scan.hasNextInt()){
                length = scan.nextInt();
                scan.nextLine();
                if(length >=2 && length <=25){
                    loopControl = false;
                } else{
                    System.out.println("# outside of range");
                }
            } else {
                System.out.println("not an int");
                scan.nextLine();
            }
        } while (loopControl);
        return length;
    }


}
