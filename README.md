# Rotate-Matrix

You are given a n x n 2D matrix A representing an image.

Rotate the image by 90 degrees (clockwise).

You need to do this in place.

Note: If you end up using an additional array, you will only receive partial score.

**Solution**

public class Solution {

    public void solve(int[][] A) {
        int n =A.length;
        int C[][]= new int[n][n];
        for(int i=0;i<n;i++)
        {
            for(int j = i;j<n;j++)
            {
                int temp= A[i][j];
                A[i][j] = A[j][i];
                A[j][i]=temp;

            }
        }
        for(int i=0;i<n;i++)
        {
           int l =0;
           int r= n-1;
           while(l<r)
           {
               int temp= A[i][l];
                A[i][l] = A[i][r];
                A[i][r]=temp;
                l++;
                r--;

           } 
        }
       /* for(int i=0;i<n;i++)
        {
            
            for(int j = 0;j<n;j++)
            {
               System.out.print(A[i][j]);
            }
        }*/

    }
}
