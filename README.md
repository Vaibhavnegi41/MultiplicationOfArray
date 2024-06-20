import java.util.*;
class multiply{
    multiply(int[][] a,int r1,int c1,int[][] b ,int r2,int c2){
        int[][] mul =new int[r1][c2];
        if(c1!=r2){
            System.out.println("Multiplication is not possible in this case ! ");
            return;
        }
        for (int i=0;i<r1;i++){
            for (int j=0;j<c2;j++){
                for (int k=0;k<c1;k++){
                    mul[i][j]+=(a[i][k]*b[k][j]);
                }
            }
        }
        System.out.println("Multiplication of two array ------- ");
        for (int i=0;i<r1;i++){
            for (int j=0;j<c2;j++){
                System.out.print(mul[i][j]+"  ");
            }
            System.out.println(" ");

        }
    }
}
public class multiplicationArray {
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        System.out.print("Enter Row of array 1 = ");
        int r1=sc.nextInt();
        System.out.print("Enter Column of array 1 = ");
        int c1=sc.nextInt();
        int [][] a=new int[r1][c1];
        for (int i=0;i<r1;i++){
            for (int j=0;j<c1;j++){
                System.out.print("Enter element = ");
                a[i][j]=sc.nextInt();
            }
        }
        for (int i=0;i<r1;i++){
            for (int j=0;j<c1;j++){
                System.out.print(a[i][j]+"  ");
            }
            System.out.println(" ");
        }
        System.out.print("Enter Row of array 2 = ");
        int r2=sc.nextInt();
        System.out.print("Enter Column of array 2 = ");
        int c2=sc.nextInt();
        int [][] b=new int[r2][c2];
        for (int i=0;i<r2;i++){
            for (int j=0;j<c2;j++){
                System.out.print("Enter element = ");
                b[i][j]=sc.nextInt();
            }
        }
        for (int i=0;i<r2;i++){
            for (int j=0;j<c2;j++){
                System.out.print(b[i][j]+"  ");
            }
            System.out.println(" ");
        }
        multiply obj=new multiply(a,r1,c1,b,r2,c2);
    }

}
