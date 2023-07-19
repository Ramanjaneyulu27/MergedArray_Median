# MergedArray_Median
Example 1:

Input: nums1 = [1,3], nums2 = [2]
Output: 2.00000
Explanation: merged array = [1,2,3] and median is 2.
Example 2:

Input: nums1 = [1,2], nums2 = [3,4]
Output: 2.50000
Explanation: merged array = [1,2,3,4] and median is (2 + 3) / 2 = 2.5.
//////CODE STARTS FROM HERE///////

public class Sortedmedian {

	public static void main(String[] args) {
		        int num[]= {1,3};
	          int num1[] = {2,4};
	          int merged[]=new int[num.length+num1.length];
	    	    for(int j=0;j<num.length;j++)
	    	    {
	    		  merged[j]=num[j];
	    		  }
	    		  for(int h=0;h<num1.length-1;h++)
	    		  { 	
	    		  for(int k=0;k<merged.length;k++)
	    		  {
	    		  if(merged[k]==0){
	    		  merged[k]=num1[h];
	            h=h+1;
	    		  }
	    		  }
	    		  }
	    		  int temp;
	    	    for(int h=0;h<merged.length;h++) {
	    	    for(int j=h;j<merged.length;j++) {
	    	    if(merged[h]>merged[j]) {
	    	    temp=merged[h];
	    	    merged[h]=merged[j];
	    	    merged[j]=temp;
	    	    }
	          }
	    	    }
	    	    System.out.print("Merged array:- ");
	    	    for(int x:merged)
	    	    {
	    		  System.out.print(+x+" ");
	    	    }
	    	    System.out.println();
	    	    int sum=0;
	    	    for(int i=0;i<merged.length;i++)
	    	    {
	    		  sum=sum+merged[i];
	    	    }
	    	    double median;
	    	    median=(double)(sum)/merged.length;
	    	    System.out.print("median is:- "+median);
            }
            }
/////FOR THE LINES OF (34-40), YOU CAN USE A SINGLE STATEMENT (Arrays.sort(merged))/////
