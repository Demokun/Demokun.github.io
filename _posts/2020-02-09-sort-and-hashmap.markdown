## 快速排序
1. 找中轴
	a. 指定一个中轴(最左边)
	b. 从右往左找，右边赋值到左边
	c. 从左往右找，左边赋值到右边
	publib int getIndex(int[] nums, int left, int right) {
		int pivot = nums[left];
		while(left < right) {
			while(nums[right] > pivot && left < right) {
				right --;
			}
			nums[left] = nums[right];
			while(nums[left] < pivot && left < right) {
				left ++;
			}
			nums[right] = nums[left];

		}
		nums[left] = pivot;
		return left;
	}
2. 左边递归，右边递归
	public void  quick_sort(int[] nums, int left, int right) {
		if(left < right) {
			int index = getIndex(int[] nums, int left, right);
			quick_sort(nums, left, index - 1);
			quick_sort(nums,index + 1, right);
		}
	}
## 哈希表
1. 创建
Map<Integer, Integer> map = new HashMap<>();
2. 查找key是否存在
Integer key;
map.containsKey(key);
3.添加键值对
map.put(key,value);
4.得到对应的key
map.get(value) 

