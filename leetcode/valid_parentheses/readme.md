# 2020春招名企就业前端工程师考点解析

BATJTMD
1. 面试题，将基础知识，前端业务，大厂面试的风格及准备方案
2. 将知识升级 知其一，其二，知三，知四，知识需要形成网络，合纵连横
3. 需要有一定的前端基础 VUE/REACT 全家桶 算法 计算机网络 操作系统 ……

### 算法核心  leetcode 

- 开始 有效括号简单算法题

给定一个只包括 '('，')'的字符串，判断字符串是否有效。注：空字符串属于有效字符串
leetcode 20 
    有效括号， 使用栈，左边括号入栈，右边括号出栈，最后判断为空
    当右边口号， 没有栈的左边括号元素，提前判端不是有效括号

- 优化一下？
    时间复杂度空间复杂度
    空间复杂度变为O(1)

面试官的出题想法是什么？
考算法， 通过算法了解同学的基础算法能力，以及思维很重要


- 最长匹配长度
32题 hard
动态规划思想
        给定一个只包含 '(' 和 ')' 的字符串，找出最长的包含有效括号的子串的长度。
        输入: "(()"
        输出: 2
        解释: 最长有效括号子串为 "()"
        示例 2:

        输入: ")()())"
        输出: 4
        解释: 最长有效括号子串为 "()()"
1. 暴力法
使用嵌套循环 每位符号（外重循环）， 它的最大长度是多少（内存循环），tmpMax。
求MAX
时间复杂度为O（n^2)
2. 将时间复杂度降下来
tmpMax 来计算 ，左右括号， 下标之间做减法，得出长度

s = "( ) ) ( ( ) )"，
一次遍历？ i 下标 0开始
提前在栈里面放一个-1 哨兵元素 0 - （-1）
） 消消乐？ 栈为空的时候， 提前退出 2 前面匹配的长度
省循环的根本 退出了再来一次

面试官 从有效括号 到最大有效长度
学习算法， 有没有专门思考或训练 easy-hard
空间复杂度，时间复杂度

- 最后
优化？  存下标，时间复杂度O（n）不太可能了 
空间复杂度？ stack O（n) -》O(1)
用变量代替栈 left right O(2)
1. () 2*right max
2. left>right    < 有效匹配结束 left==right=0


