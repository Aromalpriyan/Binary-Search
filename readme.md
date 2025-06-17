# 03 Work
# Binary Search
```
import java.util.Scanner;

public class binarySearch{

    public static void main(String[] args) {
    int[] sortedArr=new int[100];
    for(int i = 0; i<=sortedArr.length-1;i++){
    sortedArr[i]=i+1;
    }
    Scanner sc = new Scanner(System.in);
System.out.println("Enter your target number: ");
int target=sc.nextInt();
int result = binarySearch(sortedArr, target);
if(result==-1){
    System.out.println("The target is not found in the array");
}else{
    System.out.println("Element found at the index: " + result);
}
       
        }
        public static int binarySearch(int[] sortedArr,int target){
        int low =0;
        int high = sortedArr.length-1;
        while(low<=high){
            int mid = (low + high)/2;
            if (sortedArr[mid]==target){
                return mid;
            }
            if(sortedArr[mid]<target){
                low = mid +1;
            }else{
                high = mid -1;
            }
        }
        return -1;

        }
    }
```
[githublink](https://github.com/Aromalpriyan/Binary-Search)