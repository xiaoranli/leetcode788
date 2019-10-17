# 14、leetcode788、旋转数字
解法一：
--  
思路：
--
    好数的标准就是包含2，5，6，9中的至少一个（保证翻转后数值不同）并且不能包含3,4,7。    
代码： 
--
<pre>
/**
 * @author lihe
 * @date 2019/10/17 15:36
 * @descriptor
 */
public class RotatedDigits_788 {

    public int rotatedDigits(int N) {
        int count = 0;
        for(int i = 1;i <= N;i++){
            String str = String.valueOf(i);
            if((str.contains("2") || str.contains("5") || str.contains("6") || str.contains("9")) && (!str.contains("3") && !str.contains("4") && !str.contains("7")))
                count++;
        }
        return count;
    }
}
</pre>
