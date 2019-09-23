import java.io.*;
import java.util.*;

class matrix {
	public static void main (String[] args) {
		Scanner sc = new Scanner(System.in);
		int testcase = sc.nextInt();
	while(testcase-- > 0){
		    int n = sc.nextInt();
		    int a[][] = new int[n][n];
		   for(int i = 0;i<n;i++){
		        for(int j = 0;j<n;j++){
		            a[i][j] = sc.nextInt();
		        }
		    }
		    
		    inter obj = new inter();
		    System.out.println(obj.columnWithMaxZero(a, n));
		}
	}
}
}

class inter{
    
    static int columnWithMaxZero(int a[][],int n)
    {int arr[] = new int[n];

for(int i = 0 ; i < n ;i++)
{
for(int j = 0 ; j < n ;j++ )
{
if(a[i][j] == 0)
arr[j]++;
}
}
int max = 0;
int temp =0;
for(int i = 0 ; i < n ;i++)
{
if(arr[i] > max)
max = arr[i];
}
for(int i = 0 ; i < n ;i++)
{
if(arr[i] == max)
{
temp = i;
break;
}
}
return temp;
}
}
