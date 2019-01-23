题解：emmm想的有点麻烦了其实，被题目中的“你不能重复利用这个数组中同样的元素”绕进去了然后报错了两次，其实这题挺简单的就两层循环遍历数组返回下标来着

```java
public class TwoNum {
    public int[] twoSum(int[] nums, int target) {
        int[] result=new int[2];
        for (int i=0;i<nums.length;i++)
        {
            for (int j=i+1;j<nums.length;j++)
            {
                if (target==nums[i]+nums[j])
                {
                    result[0]=i;
                    result[1]=j;
                    break;
                }
            }
        }
        return result;
    }
}
```