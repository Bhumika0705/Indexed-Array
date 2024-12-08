# Indexed-Array
import java.util.Scanner;

public class IndexedArray {
    public IndexedArray() {
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the Dimensions of Array:");
        int n = sc.nextInt();
        int[] arr = new int[n];
        System.out.println("Enter the elements of Array:");

        int target;
        for(target = 0; target < n; ++target) {
            arr[target] = sc.nextInt();
        }

        System.out.println("Enter the target:");
        target = sc.nextInt();
        int i = 0;
        int j = n - 1;

        while(i < j) {
            if (arr[i] + arr[j] == target) {
                ++i;
                ++j;
                System.out.println("" + i + " " + j);
                return;
            }

            if (arr[i] + arr[j] > target) {
                --j;
            } else {
                ++i;
            }
        }

        System.out.println(-1);
    }
}
