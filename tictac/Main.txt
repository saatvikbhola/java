import java.util.LinkedHashMap;
import java.util.Map;

public class Main{

    //hashmap used to store the values of x and o
    //char used to respond to which box it will be stored in
    static Map<String, Character> board = new LinkedHashMap<>();
    static char[] brd_keys = {'7','8','9','4','5','6','1','2','3'};


    static void print_board(Map<String, Character> board){
        System.out.println(" ");
        System.out.println("\t"+"  "+board.get("7")+"  "+"|"+"  "+board.get("8")+"  "+"|"+"  "+board.get("9")+"  ");
        System.out.println("\t-----"+"+"+"-----"+"+"+"-----");
        System.out.println("\t"+"  "+board.get("4")+"  "+"|"+"  "+board.get("5")+"  "+"|"+"  "+board.get("6")+"  ");
        System.out.println("\t----" +
                "-"+"+"+"-----"+"+"+"-----");
        System.out.println("\t"+"  "+board.get("1")+"  "+"|"+"  "+board.get("2")+"  "+"|"+"  "+board.get("3")+"  ");
    }

    public static void clearScreen() {
        for (int i = 0; i < 50; i++) {
            System.out.println();
        }
    }

    public static void main(String[] args){

        for (char key : brd_keys){
            board.put(String.valueOf(key), ' ');
        }

        print_board(board);
        board.put("7",'x');
        print_board(board);
        board.put("5",'x');
        print_board(board);
    }

}