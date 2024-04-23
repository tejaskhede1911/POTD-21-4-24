# POTD-21-4-24
**Three way partitioning**

class Solution
{
    public void swap(int arr[], int i, int j) 
    {
        int temp = arr[i];
        arr[i] = arr[j];
        arr[j] = temp;
    }
    
    public void threeWayPartition(int arr[], int a, int b)
    {
        int n = arr.length, i = 0, l = 0, r = n - 1;
        
        while(i <= r) 
        {
            if(arr[i] < a)
            {
                swap(arr, l, i);
                l++;
            }
            
            else if(arr[i] > b)
            {
                swap(arr, i, r);
                r--;
                i--;
            }
            
            i++;
        }
    }
}

Input: 
n = 5
array[] = {1, 2, 3, 3, 4}
[a, b] = [1, 2]
Output: 
1
Explanation: 
One possible arrangement is: {1, 2, 3, 3, 4}. If you return a valid arrangement, output will be 1.
