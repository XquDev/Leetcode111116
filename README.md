# Leetcode111116


# Array
This branch is about Array operation.

#.448. Find All Numbers Disappeared in an Array.
(No extra space and T(n)=O(n))

1. Swap each pair of numbers, and make the array in right order, then compare the elements with index.(Used)
2. Mark each number with -1, the index in the new array which is positive are the answers.()

    	for(int i= 0; i<nums.length; i++){//n
    	    while(nums[i] != i+1 && nums[i] != nums[nums[i]-1]){
    	        int temp = nums[i];
    	        nums[i] = nums[temp-1];
    	        nums[temp-1] = temp;
    	    }
    	}
      //while condition: Make sure the number in right position and two equal numbers would not have been swapped. 
      

    十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十

#.442. Find All Duplicates in an Array.
(No extra space and T(n)=O(n))

1. Sorted the array first, then find the duplicated numbers.(Used)O(nlog(n)
2. Mark each number with -1.
        for(int i= 0;i<nums.length;i++){
            int temp = Math.abs(nums[i]);
            if(nums[temp-1] < 0)
                res.add(temp);
            else
                nums[temp-1] = -1 * nums[temp-1];
        }
    
    十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十十
