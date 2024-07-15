# firstRepo
It is my first repository in Github.
//Binary Search
import java.util.*;
import java.util.Scanner;
class BinarySearch
{
	static int binSearch(int[] arr,int target)
	{
		int start=0;
		int end=arr.length-1;
		while(start<=end)
		{
			int mid=(start+end)/2;
			if(target==arr[mid])
			{
				return mid;
			}
			if(target<arr[mid])
			{
				end=mid-1;
			}
			else
			{
				start=mid+1;
			}
		}
		return -1;
	}
	public static void main(String args[])
	{
		int[] arr={0,1,6,45,49,52,65};
		Scanner s=new Scanner(System.in);
		System.out.println("Enter element to search:");
		int target=s.nextInt();
		int index=binSearch(arr,target);
		System.out.println("Element at index:"+index);
	}
}
