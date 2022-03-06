# Chess-warner-
Chess Knight,rook,bishop warner  
import java.util.Scanner;
public class Chess {

    public static void main (String[] args) {

        final int MAX_ROW_COL=8,MIN_ROW_COL=1;
        char first,second;
        int row1,col1,row2,col2,threats=0; 

        Scanner scan = new Scanner(System.in);
        System.out.println("Please enter the type"+
            " of the first chessman");
        first = scan.next().charAt(0);
        System.out.println ("Please enter the number of row");
        row1 = scan.nextInt();
        System.out.println ("Please enter the number of column");
        col1 = scan.nextInt();
        System.out.println("Please enter the type"+
            " of the second chessman");
        second = scan.next().charAt(0);
        System.out.println ("Please enter the number of row");
        row2 = scan.nextInt();
        System.out.println ("Please enter the number of column");
        col2 = scan.nextInt(); 

        if (first==second)
        {
            System.out.println ("Chessmen should be different from each other"); 
        }

        if((row1<MIN_ROW_COL) || (row1>MAX_ROW_COL) || (col1<MIN_ROW_COL) || (col1>MAX_ROW_COL))
            System.out.println("Position is not Legal"); 

        if((row2<MIN_ROW_COL) || (row2>MAX_ROW_COL) || (col2<MIN_ROW_COL) || (col2>MAX_ROW_COL))           
        {
            System.out.println("Position is not Legal");
        }

        if(row1==row2)
        {
            if (col1==col2)
            {
                System.out.println("Chessmen positions should not be identical");
            }
        }

        if(((first=='b') && (second=='r')) || ((first=='r') && (second=='b') )) //rook threats bishop
        {

            if((row1==row2) || (col1==col2))
            {

                threats=1; 
                System.out.println("rook threat bishop");
            }
        }

        if(((first=='r') && (second=='k'))  || (first=='k') && (second=='r'))//rook threats knight
        {
            if((row1==row2) || (col1==col2))
                threats=1; 
            System.out.println("rook threat knight");

        }

        if((first=='k') && (second=='r') || (first=='r') && (second=='k')) //knight  threats rook 
        {

            if((row1-2==row2) && (col1-1==col2))
            {
                threats=1; 
                System.out.println("knight threats rook");}
            if((row1-2==row2) && (col1+1==col2)){
                threats=1; 
                System.out.println("knight threats rook");}
            if((row1+2==row2) && (col1-1==col2)){
                threats=1; 
                System.out.println("knight threats rook");}
            if((row1+2==row2) && (col1+1==col2)){
                threats=1; 
                System.out.println("knight threats rook");}
            if((row1+1==row2) && (col1+2==col2)){
                threats=1; 
                System.out.println("knight threats rook");}
            if((row1+1==row2) && (col1-2==col2)){
                threats=1; 
                System.out.println("knight threats rook");}
            if((row1-1==row2) && (col1+2==col2)){
                threats=1; 
                System.out.println("knight threats rook");}
            if((row1-1==row2) && (col1-2==col2)){
                threats=1; 
                System.out.println("knight threats rook");}
        }

        if((first=='k') && (second=='b') || (first=='b') && (second=='k')) //knight  threats bishop 
        {

            if((row1-2==row2) && (col1-1==col2)){
                threats=1;
                System.out.println("knight threats bishop");}
            if((row1-2==row2) && (col1+1==col2)){
                threats=1; 
                System.out.println("knight threats bishop");}
            if((row1+2==row2) && (col1-1==col2)){
                threats=1; 
                System.out.println("knight threats bishop");}
            if((row1+2==row2) && (col1+1==col2)){
                threats=1; 
                System.out.println("knight threats bishop");}
            if((row1+1==row2) && (col1+2==col2)){
                threats=1; 
                System.out.println("knight threats bishop");}
            if((row1+1==row2) && (col1-2==col2)){
                threats=1; 
                System.out.println("knight threats bishop");}
            if((row1-1==row2) && (col1+2==col2)){
                threats=1; 
                System.out.println("knight threats bishop");}
            if((row1-1==row2) && (col1-2==col2)){
                threats=1; 
                System.out.println("knight threats bishop");}
        }

        if(((first=='b') && (second=='k')) || ((first=='k') && (second=='b'))) //bishop threats knight
        { //first slant (possitive)
            if((row2-7==row1) && (col2-7==col1)){

                threats=1; 
                System.out.println("bishop threats knight");}
            if((row2-6==row1) && (col2-6==col1)){
                threats=1; 
                System.out.println("bishop threats knight");}
            if((row2-5==row1) && (col2-5==col1)){
                threats=1; 
                System.out.println("bishop threats knight");}
            if((row2-4==row1) && (col2-4==col1)){
                threats=1; 
                System.out.println("bishop threats knight");}
            if((row2-3==row1) && (col2-3==col1)){
                threats=1; 
                System.out.println("bishop threats knight");}
            if((row2-2==row1) && (col2-2==col1)){
                threats=1; 
                System.out.println("bishop threats knight");}
            if((row2-1==row1) && (col2-1==col1)){
                threats=1; 
                System.out.println("bishop threats knight");}
            if((row2+0==row1) && (col2+0==col1)){
                threats=1; 
                System.out.println("bishop threats knight");}
            if((row2+1==row1) && (col2+1==col1)){
                threats=1; 
                System.out.println("bishop threats knight");}
            if((row2+2==row1) && (col2+2==col1)){
                threats=1; 
                System.out.println("bishop threats knight");}
            if((row2+3==row1) && (col2+3==col1)){
                threats=1; 
                System.out.println("bishop threats knight");}
            if((row2+4==row1) && (col2+4==col1)){
                threats=1; 
                System.out.println("bishop threats knight");}
            if((row2+5==row1) && (col2+5==col1)){
                threats=1; 
                System.out.println("bishop threats knight");}
            if((row2+6==row1) && (col2+6==col1)){
                threats=1; 
                System.out.println("bishop threats knight");}
            if((row2+7==row1) && (col2+7==col1)){
                threats=1; 
                System.out.println("bishop threats knight");}
            //second slant
            if((row2-7==row1) && (col2-0==col1)){
                threats=1;
                System.out.println("bishop threats knight");}
            if((row2-6==row1) && (col2-1==col1)){
                threats=1;
                System.out.println("bishop threats knight");}
            if((row2-5==row1) && (col2-2==col1)){
                threats=1;
                System.out.println("bishop threats knight");}
            if((row2-4==row1) && (col2-3==col1)){
                threats=1;
                System.out.println("bishop threats knight");}
            if((row2-3==row1) && (col2-4==col1)){
                threats=1;
                System.out.println("bishop threats knight");}
            if((row2-2==row1) && (col2-5==col1)){
                threats=1;
                System.out.println("bishop threats knight");}
            if((row2-1==row1) && (col2-6==col1)){
                threats=1;
                System.out.println("bishop threats knight");}
            if((row2+0==row1) && (col2+7==col1)){
                threats=1;
                System.out.println("bishop threats knight");}
            if((row2+1==row1) && (col2+6==col1)){
                threats=1;
                System.out.println("bishop threats knight");}
            if((row2+2==row1) && (col2+5==col1)){
                threats=1;
                System.out.println("bishop threats knight");}
            if((row2+3==row1) && (col2+4==col1)){
                threats=1;
                System.out.println("bishop threats knight");}
            if((row2+4==row1) && (col2+3==col1)){
                threats=1;
                System.out.println("bishop threats knight");}
            if((row2+5==row1) && (col2+2==col1)){
                threats=1;
                System.out.println("bishop threats knight");}
            if((row2+6==row1) && (col2+1==col1)){
                threats=1;
                System.out.println("bishop threats knight");}
            if((row2+7==row1) && (col2+0==col1)){
                threats=1;
                System.out.println("bishop threats knight");}
        }

        if(((first=='b') && (second=='r'))||((first=='r') && (second=='b'))) //bishop threats rook   
        {

            //first slant
            if((row2-7==row1) && (col2-7==col1))
            {
                threats=1;
                System.out.println("bishop threats rook");}

            if((row2-6==row1) && (col2-6==col1)){
                threats=1;
                System.out.println("bishop threats rook");}
            if((row2-5==row1) && (col2-5==col1)){
                threats=1;
                System.out.println("bishop threats rook");}
            if((row2-4==row1) && (col2-4==col1)){
                threats=1;
                System.out.println("bishop threats rook");}
            if((row2-3==row1) && (col2-3==col1)){
                threats=1;
                System.out.println("bishop threats rook");}
            if((row2-2==row1) && (col2-2==col1)){
                threats=1;
                System.out.println("bishop threats rook");}
            if((row2-1==row1) && (col2-1==col1)){
                threats=1;
                System.out.println("bishop threats rook");}
            if((row2+0==row1) && (col2+0==col1)){
                threats=1;
                System.out.println("bishop threats rook");}
            if((row2+1==row1) && (col2+1==col1)){
                threats=1;
                System.out.println("bishop threats rook");}
            if((row2+2==row1) && (col2+2==col1)){
                threats=1;
                System.out.println("bishop threats rook");}
            if((row2+3==row1) && (col2+3==col1)){
                threats=1;
                System.out.println("bishop threats rook");}
            if((row2+4==row1) && (col2+4==col1)){
                threats=1;
                System.out.println("bishop threats rook");}
            if((row2+5==row1) && (col2+5==col1)){
                threats=1;
                System.out.println("bishop threats rook");}
            if((row2+6==row1) && (col2+6==col1)){
                threats=1;
                System.out.println("bishop threats rook");}
            if((row2+7==row1) && (col2+7==col1)){
                threats=1;
                System.out.println("bishop threats rook");}

            //second slant   
            if((row2-7==row1) && (col2-0==col1)){
                threats=1;
                System.out.println("bishop threats rook");}
            if((row2-6==row1) && (col2-1==col1)){
                threats=1;
                System.out.println("bishop threats rook");}
            if((row2-5==row1) && (col2-2==col1)){
                threats=1;
                System.out.println("bishop threats rook");}
            if((row2-4==row1) && (col2-3==col1)){
                threats=1;
                System.out.println("bishop threats rook");}
            if((row2-3==row1) && (col2-4==col1)){
                threats=1;
                System.out.println("bishop threats rook");}
            if((row2-2==row1) && (col2-5==col1)){
                threats=1;
                System.out.println("bishop threats rook");}
            if((row2-1==row1) && (col2-6==col1)){
                threats=1;
                System.out.println("bishop threats rook");}
            if((row2+0==row1) && (col2+7==col1)){
                threats=1;
                System.out.println("bishop threats rook");}
            if((row2+1==row1) && (col2+6==col1)){
                threats=1;
                System.out.println("bishop threats rook");}
            if((row2+2==row1) && (col2+5==col1)){
                threats=1;
                System.out.println("bishop threats rook");}
            if((row2+3==row1) && (col2+4==col1)){
                threats=1;
                System.out.println("bishop threats rook");}
            if((row2+4==row1) && (col2+3==col1)){
                threats=1;
                System.out.println("bishop threats rook");}
            if((row2+5==row1) && (col2+2==col1)){
                threats=1;
                System.out.println("bishop threats rook");}
            if((row2+6==row1) && (col2+1==col1)){
                threats=1;
                System.out.println("bishop threats rook");}
            if((row2+7==row1) && (col2+0==col1)){
                threats=1;
                System.out.println("bishop threats rook");}
        }
        if(threats==0)
            System.out.println("no threat");
    }
}  

