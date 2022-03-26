# Kombinasyon-Hesaplayan-Program
Patika.dev > Java101 > Döngüler > Pratik4 - Kombinasyon Hesaplayan Program

Java ile faktöriyel hesaplayan program yazıyoruz.

### Ödev
N elemanlı bir kümenin elemanları ile oluşturulacak r elemanlı farklı grupların sayısı n’in r’li kombinasyonu olarak adlandırılır. N’in r’li kombinasyonu C(n,r) şeklinde gösterilir.

Java ile kombinasyon hesaplayan program yazınız.

#### Kombinasyon formülü
C(n,r) = n! / (r! * (n-r)!)


      import java.util.*;

      public class combination {

        public static void main(String[] args) {

          Scanner sc = new Scanner(System.in);

          System.out.print("Enter the n: ");
          int n = sc.nextInt();

          System.out.print("Enter the r: ");
          int r = sc.nextInt();

          int n_fac = 1;
          for(int i = 1; i < n; i++) {
            i *= n_fac;
          }

          int r_fac = 1;
          for(int i = 1; i < r; i++) {
            i *= r_fac;
          }

          int diff_fac = 1;
          for(int i = 1; i < (n-r); i++) {
            i *= diff_fac;
          }

          System.out.println("r combination of n is " + (n_fac / (r_fac * diff_fac)));
        }
      }
