public class Euclid{
    // recursive inplementation
    public static int gcd(int x, int y){
        if(y == 0) return x;
        else 
        {
            return gcd(y, x % y);
        }
    }
    // non-recursive implementation
    public static int gcd2(int x, int y){
    while(y != 0){
        int temp = y;
        y = x % y;
        x = temp;
    }
    return x;
    }
    public static void main(String[] args){
        int x = Integer.parseInt(args[0]);
        int y = Integer.parseInt(args[1]);
        int d  = gcd(x, y);
        int d2 = gcd2(x,y);
        System.out.println("gcd(" + x + ", " + y + ") = " + d);
        System.out.println("gcd(" + x + ", " + y + ") = " + d2);
    }
}