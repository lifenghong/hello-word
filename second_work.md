## 题目
> Given an array and a value, remove all instances of that value in-place and return the new length.

> Do not allocate extra space for another array, you must do this by modifying the input array in-place with O(1) extra memory.

> The order of elements can be changed. It doesn't matter what you leave beyond the new length.
## 例子
> Example:

> Given nums = [3,2,2,3], val = 3,

> Your function should return length = 2, with the first two elements of nums being 2.
## 问题分析
#### 题目要求不要为其他数组分配额外空间，但要求通过数组来实现，一开始我使用单纯数组来解决，比较麻烦，耗时较长，我先定义了一个比较小的数组，然后将删掉元素的数组重新赋值给这个较小的数组。再计算小数组的长度。参考了别人的答案，学会了一种新的用法：vector，vector在数组元素插入，删除方面，应用起来比较方便。
## 代码实现：
```
c++:
#include<iostream>
#include<vector>
using namespace std;
    int removeElement(vector<int>& nums, int val) {
        int id=0;
        for(int i = 0;i<nums.size();i++)
        {
            if(nums[i]!=val)
                nums[id++]=nums[i];
        }
        return id;
    }

    int main()
    {
    	vector<int> num(4,0);
    	int m;
    	for(int i=0;i<4;i++)
    	cin>>num[i];
    	cin>>m;
    	cout<<removeElement(num,m);
    	return 0;
	}
  ```
  
