## String  

1. String判空  

````java
	String s;
	if(s == null || s.length() <= 0) {

	}
````
2. String和char[]类型转换  

	
	String转char[]:toCharArray()  

````java
	String s;
	char[] cs = s.toCharArray();
````
	char[]转String：valueOf()  

````java
	char[] cs = {'h','e','l','l','o','w','o','r','l','d'};
	String s = cs.valueOf(cs);
````
3. 长度  
````java
	String s;
	s.length();
````
## stack  

stack s;  

s.isEmpty();  

s.peek();  

s.pop();  

s.push();  

## if - else 和 if - else if - else  

## && 和 ||优先级  

先执行&&再执行||  

## 链表类先初始化再指定next  

````java
	public ListNode() {
		int val;
		ListNode next;
		ListNode(int x) {val = x};
	}
````
错误使用：  

````java
	ListNode target = new ListNode(1);
	ListNode node;
	node.next = target; //报错：空指针
````
正确使用：  

````java
	ListNode target = new ListNode(1);
	ListNode node = new ListNode(2);
	node.next = target;
````
