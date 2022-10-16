import java.util.*;
interface AdvancedArithmetic{
  int divisor_sum(int n);
}
 
class Solution{
    public static void main(String []args){
        
        class MyCalculator implements  AdvancedArithmetic{
    public MyCalculator() {
    }
 
    public int divisor_sum(int n) {
        int result=0;
        for ( int i =1 ; i<=n; i++){
            
            if (n%i ==0){
                System.out.println(i+" Es divisor de "+n);
                result=result+i;
            }else {
                System.out.println(i+" No divisor de "+n);
            }                      
        } 
        return result;
      }   
};
        
        MyCalculator my_calculator = new MyCalculator();
        System.out.print("I implemented: ");
        ImplementedInterfaceNames(my_calculator);
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        System.out.print(my_calculator.divisor_sum(n) + "\n");
        sc.close();
    }

    static void ImplementedInterfaceNames(Object o){
        Class[] theInterfaces = o.getClass().getInterfaces();
        for (int i = 0; i < theInterfaces.length; i++){
            String interfaceName = theInterfaces[i].getName();
            System.out.println(interfaceName);
        }
    }
}
