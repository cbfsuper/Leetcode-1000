#### leetCode-225.用队列实现栈
思路: 队列q进入一个元素x时，将队列q中除了x以外的所有元素出队再入队
##### 编程之美-3.7 最小队列
题目描述: 要求O(1)时间获得当前队列中的最小(大)值   
思路：解法(1)：堆,将所有元素放进最小/大堆中，入队、出队时间复杂度为O(logN)    
解法(2)：用两个栈s1、s2实现队列，那么队列的最小值就是min(s1.min(), s2.min())，入队、出队时间复杂度为O(1)  
上述两种方法都是通过空间换时间达到了获取当前队列最小值时间复杂度为O(1)
>最大队列呢