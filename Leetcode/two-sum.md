
https://leetcode.com/problems/two-sum/

説明
-------------
配列をループ処理しながら、2つの数の和がtargetと一致する場合、そのインデックスをanswerに格納し、breakでループを抜け出しました。

```Csharp
public class Solution {
    public int[] TwoSum(int[] nums, int target) {
        int[] answer = {0,0};
        for (int i=0; i<nums.Length-1; i++) {
            for (int j=1; j<nums.Length; j++) {
                if (nums[i] + nums[j] == target) {
                    answer[0] = i;
                    answer[1] = j;
                    break;
                }
            }
        }
        return answer;
    }
}
```
