```java
class Solution {
    public int search(int[] nums, int target) {
        int low =0;
        int high = nums.length - 1;
        int result = -1;

        while(low <= high) {
            int mid = (low + high) / 2;
            if(nums[mid] == target) {
                result = mid;
                break;
            }
            else if(nums[mid] < target) {
                low = mid + 1;
            } else if(nums[mid] > target) {
                high = mid - 1;
            }
        }
        return result;
    }
}
```
![image](https://user-images.githubusercontent.com/43237961/227120400-4d5f5ef6-e422-4a4e-b8b8-581b6b590a2e.png)
<br> 
binary search's time complexity is  O(logN) <br>
It is better solving it by using loop (ex. while) than using recursion. <br> 
And it is important binary search is always sorted and it is for short list rather than long list. <br>
