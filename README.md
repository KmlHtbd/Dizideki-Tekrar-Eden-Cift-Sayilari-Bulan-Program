# Dizideki-Tekrar-Eden-Cift-Sayilari-Bulan-Program
---
Bu bir [patika.dev](www.patika.dev) projesidir.
```
import java.util.Arrays;

public class RepeatEvenFind {
    static  boolean isFind(int arr[], int value){
        for (int i:arr){
            if(value==i){
                return true;
            }
        }return false;
    }
    public static void main(String[] args) {
        int[] list = {1,9,1,2,66,2,3,4,98,73,66,9,33,98};
        int[] duplicate = new int[list.length];
        int startindex  =0;

        for(int i=0;i<list.length;i++){
            for(int j=0;j< list.length;j++){
                if ((i!=j) && (list[i]==list[j])){
                    if (!isFind(duplicate,list[i])){
                        duplicate[startindex++] = list[i];
                        break;
                    }
                }
            }
        }
        for (int i:duplicate){
            if (i!=0 && i%2==0){
                System.out.println(i);
            }
        }
    }
}
```
