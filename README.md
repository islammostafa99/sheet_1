# sheet_1
sheet1
public static void inverse(int[] arr){
	int i,k;
	for (i=0;i<(arr.length/2);i++) {
            k=arr[i];
            arr[i] = arr[arr.length-i-1];
            arr[arr.length-i-1]=k;
        }
}

public static int[] sumEvenOdd(int[] a){
        int j;
        int[] c= new int[2];
        c[0]=0;
        c[1]=0;
        for (j = 0;j<a.length;j++) {
            if(a[j]%2==0){
                c[0]+=a[j];
            }else{
                c[1]+=a[j];
            }
        }
        return c;
}

public static double average(int[] a){
        int j;
        long k=0;
        for(j=0;j<a.length;j++){
            k+=a[j];
        }
        return (double)k/a.length;
}

public static void moveValue(int[] arr,int val) {
        int j, c, b = 0, d;
        for (j = 0; j < arr.length; j++) {
            if (val == arr[j]) {
                for (b = j; b < arr.length - 1; b++) {
                    for (d = j + 1; d < arr.length; d++) {
                        if (arr[b] == val) {
                            if (arr[d] != val) {
                                c = arr[b];
                                arr[b] = arr[d];
                                arr[d] = c;
                            }
                        }
                    }
                }
            }
        }
 }


public static void transpose(int[][] arr){
        int i,j,s;
        for(i=0;i<arr.length;i++){
            for(j=0;j<arr[0].length;j++){
                if(i<j){
                    s=arr[i][j];
                    arr[i][j]=arr[j][i];
                    arr[j][i]=s;
                }
            }
        }
 }


 public static int fibonacci(int[] arr,int n){
        int i;
        arr[0]=0;
        arr[1]=1;
        for(i=2;i<n;i++){
            arr[i]=arr[i-1]+arr[i-2];
        }
        return arr[n-1];
 }
