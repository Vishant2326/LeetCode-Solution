                             ARRAY PROBLEMS
1. Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.
You may assume that each input would have exactly one solution, and you may not use the same element twice.
You can return the answer in any order.

Input: nums = [2,7,11,15], target = 9
Output: [0,1]

Explanation: Because nums[0] + nums[1] == 9, we return [0, 1].

Hint:-(N+N)

Solution:-

int* twoSum(int* nums, int numsSize, int target, int* returnSize){    
    *returnSize = 2;
    int* element = (int*)malloc(2*sizeof(int));
    for(int i=0; i<numsSize; i++)
        for(int j=i+1; j<numsSize; j++)
            if(nums[j] == target - nums[i])
            {
                printf("i = %d, j = %d\n", i, j);
                element[0] = i;
                element[1] = j;
                return element;                
            }
    // Return [-1,-1] if no result
    printf("No result with specified target\n");
    element[0] = -1;
    element[1] = -1;
    return element;
}

