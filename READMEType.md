
## 哈希表

`哈希表`拥有记数的功能，如果题目中包含字眼`至多xx次`， `至少xx次`,`唯一`等等字眼，可以联想到用哈希表来解决。

### 哈希表 + 计数类型
- [387. 字符串中的第一个唯一字符](https://github.com/PENTONCOS/leetcode/tree/main/easy/387.%20字符串中的第一个唯一字符.md)
- [242. 有效的字母异位词](https://github.com/PENTONCOS/leetcode/tree/main/easy/242.%20有效的字母异位词.md)
- [169. 多数元素](https://github.com/PENTONCOS/leetcode/tree/main/easy/169.%20多数元素.md)
- [136. 只出现一次的数字](https://github.com/PENTONCOS/leetcode/tree/main/easy/136.%20只出现一次的数字.md)

### 哈希表 + 映射功能

哈希表有一个非常常见的功能就是建立映射关系，比如说设计模式里的策略模式，思路是一样的，映射表常常见于后端的枚举类型，typescript也是一样，我们举一个js的例子

```typescript
// 后端只会返回0，1，2
const TYPE = {
    2: 'orange',
    1: 'red',
    0: 'blue'
}

// 然后前端会这样用
TYPE[后端返回的数字0或1或2]
```

- [1. 两数之和](https://github.com/PENTONCOS/leetcode/tree/main/easy/1.%20两数之和.md)
- [349. 两个数组的交集](https://github.com/PENTONCOS/leetcode/tree/main/easy/349.%20两个数组的交集.md)

## 找规律
- [13. 罗马数字转整数](https://github.com/PENTONCOS/leetcode/tree/main/easy/13.%20罗马数字转整数.md)
- [14. 最长公共前缀](https://github.com/PENTONCOS/leetcode/tree/main/easy/14.%20最长公共前缀.md)
- [21. 合并两个有序链表](https://github.com/PENTONCOS/leetcode/tree/main/easy/21.%20合并两个有序链表.md)
- [28. 实现 strStr()](https://github.com/PENTONCOS/leetcode/tree/main/easy/28.%20实现%20strStr().md)
- [118. 杨辉三角](https://github.com/PENTONCOS/leetcode/tree/main/easy/118.%20杨辉三角.md)
- [121. 买卖股票的最佳时机](https://github.com/PENTONCOS/leetcode/tree/main/easy/121.%20买卖股票的最佳时机.md)
- [122. 买卖股票的最佳时机 II](https://github.com/PENTONCOS/leetcode/tree/main/easy/122.%20买卖股票的最佳时机%20II.md)
- [206. 反转链表](https://github.com/PENTONCOS/leetcode/tree/main/easy/206.%20反转链表.md) 这个题必须掌握牢实，是解很多链接表题的基础的基础。

## 双指针
双指针是解数组类型题最常见解法

1. 比如有头尾分别有指针，然后依次向中间靠拢的双指针，
2. 还有一种是快慢是指针，两个指针都是从左边开始，一个走的快，一个走得慢

- [26. 删除有序数组中的重复项](https://github.com/PENTONCOS/leetcode/tree/main/easy/26.%20删除有序数组中的重复项.md)
- [88. 合并两个有序数组](https://github.com/PENTONCOS/leetcode/tree/main/easy/88.%20合并两个有序数组.md)
- [125. 验证回文串](https://github.com/PENTONCOS/leetcode/tree/main/easy/125.%20验证回文串.md)
- [234. 回文链表](https://github.com/PENTONCOS/leetcode/tree/main/easy/234.%20回文链表.md)
- [237. 删除链表中的节点](https://github.com/PENTONCOS/leetcode/tree/main/easy/237.%20删除链表中的节点.md)
- [283. 移动零](https://github.com/PENTONCOS/leetcode/tree/main/easy/283.%20移动零.md)
- [344. 反转字符串](https://github.com/PENTONCOS/leetcode/tree/main/easy/344.%20反转字符串.md)
- [350. 两个数组的交集II](https://github.com/PENTONCOS/leetcode/tree/main/easy/350.%20两个数组的交集II.md)

## 二叉树（DFS）
### 二叉树 前中后遍历 套路详解
前序遍历题目如下：

root节点是A节点（下图的A节点），然后让你按照下图数字的顺序依次打印出节点。

![](https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/9f23accef4a5402da0c898920e64a8f4~tplv-k3u1fbpfcp-zoom-in-crop-mark:3024:0:0:0.awebp)

我们可以看到这其中的规律，就是`深度优先遍历，先遍历左子树，再遍历右子树`，这里我们不用递归，因为一些大厂严格要求二叉树遍历不用递归，递归太简单了。

重点思路就是：`深度优先遍历，先遍历左子树，再遍历右子树`，

所以，我们需要一套如何遍历一颗二叉树，并且是先左子树，再右子树的通用模板，如下
```js
var Traversal = function(root) {
    const stack = [];
    while (root || stack.length){
      while(root){
        stack.push(root);
        root = root.left;
      }
      root = stack.pop();
      root = root.right;
    }
    return res;
};
```
我们结合图片发现这个遍历产生的整体压栈的顺序是
```
A、B、D入栈，
D出栈
B出栈
E入栈
E出栈
A出栈
C入栈
C出栈
F入栈
F出栈
```
我们把上面入栈的元素按顺序排列一下就是，A、B、D、E、C、F，而这就是前序遍历的顺序。

下面的中序遍历，我们看看出栈顺序是不是中序遍历的要求：D、B、E、A、C、F

放具体前序遍历代码：

```js
var preorderTraversal = function(root) {
    // 初始化数据
    const res =[];
    const stack = [];
    while (root || stack.length){
      while(root){
        res.push(root.val);
        stack.push(root);
        root = root.left;
      }
      root = stack.pop();
      root = root.right;
    }
    return res;
};
```
中序遍历是一个意思，在前序遍历的基础上改造一下

![](https://p6-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/2de9035c3cc1425bbb64ef5b5d821181~tplv-k3u1fbpfcp-zoom-in-crop-mark:3024:0:0:0.awebp)

```js
var preorderTraversal = function(root) {
    // 初始化数据
    const res =[];
    const stack = [];
    while (root || stack.length){
      while(root){
        stack.push(root);
        root = root.left;
      }
      root = stack.pop();
      res.push(root.val);
      root = root.right;
    }
    return res;
};
```

后序遍历有点不太一样，但是套路是一样的，我们需要先遍历右子树，再遍历左子树，反着来，就可以了，代码如下：

![](https://p1-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/e45cdd1671ed4128ad67b99631146410~tplv-k3u1fbpfcp-zoom-in-crop-mark:3024:0:0:0.awebp)

```js
var postorderTraversal = function(root) {
  // 初始化数据
    const res =[];
    const stack = [];
    while (root || stack.length){
      while(root){
        stack.push(root);
        res.unshift(root.val);
        root = root.right;
      }
      root = stack.pop();
      root = root.left;
    }
    return res;
};
```
### 对称二叉树
这个题简而言之就是判断一个二叉树是对称的，比如说：
二叉树 `[1,2,2,3,4,4,3]` 是对称的。
```
    1
   / \
  2   2
 / \ / \
3  4 4  3
```
但是下面这个 `[1,2,2,null,3,null,3]` 则不是镜像对称的:
```
    1
   / \
  2   2
   \   \
   3    3

```
思路：
递归解决：

- 判断两个指针当前节点值是否相等
- 判断 A 的右子树与 B 的左子树是否对称
- 判断 A 的左子树与 B 的右子树是否对称
```js
function isSame(leftNode, rightNode){
    if(leftNode === null && rightNode === null) return true;
    if(leftNode === null || rightNode === null) return false;
    return leftNode.val === rightNode.val && isSame(leftNode.left, rightNode.right) && isSame(leftNode.right, rightNode.left)
}
var isSymmetric = function(root) {
    if(!root) return root;
    return isSame(root.left, root.right);
};
```
### 二叉树的最大深度
这个题在面试滴滴的时候遇到过，主要是掌握二叉树遍历的套路

- 只要遍历到这个节点既没有左子树，又没有右子树的时候
- 说明就到底部了，这个时候如果之前记录了深度，就可以比较是否比之前记录的深度大，大就更新深度
- 然后以此类推，一直比较到深度最大的
```js
var maxDepth = function(root) {
    if(!root) return root;
    let ret = 1;
    function dfs(root, depth){
        if(!root.left && !root.right) ret = Math.max(ret, depth);
        if(root.left) dfs(root.left, depth+1);
        if(root.right) dfs(root.right, depth+1);
    }
    dfs(root, ret);
    return ret
};
```

- [108. 将有序数组转化为二叉搜索树](https://github.com/PENTONCOS/leetcode/tree/main/easy/108.%20将有序数组转化为二叉搜索树.md)

## 栈

栈是一种先进后出的数据结构，所以涉及到你需要`先进后出`这个想法后，就可以使用栈。

其次栈跟递归很相似，递归也是先压栈，然后先进来的先出去，就跟函数调用栈一样。


- [20. 有效的括号](https://github.com/PENTONCOS/leetcode/tree/main/easy/20.%20有效的括号.md)
- [155. 最小栈](https://github.com/PENTONCOS/leetcode/tree/main/easy/155.%20最小栈.md)
  
## 动态规划

动态规划，一定要知道动态转移方程，有了这个，就相当于解题的钥匙。

- [53. 最大子数组和](https://github.com/PENTONCOS/leetcode/tree/main/easy/53.%20最大子数组和.md)
- [70. 爬楼梯](https://github.com/PENTONCOS/leetcode/tree/main/easy/70.%20爬楼梯.md)

## 数学问题

以下更多的是涉及数学问题，这些解法非常重要，因为在中级题里面会经常用到，**中级的两数相加都是一个模板**。

- [66. 加一](https://github.com/PENTONCOS/leetcode/tree/main/easy/66.%20加一.md)
- [69. x的平方根](https://github.com/PENTONCOS/leetcode/tree/main/easy/69.%20x的平方根.md)
- [171. Excel 表列序号](https://github.com/PENTONCOS/leetcode/tree/main/easy/171.%20Excel%20表列序号.md)
- [172. 阶乘后的零](https://github.com/PENTONCOS/leetcode/tree/main/easy/172.%20阶乘后的零.md)
- [190. 颠倒二进制位](https://github.com/PENTONCOS/leetcode/tree/main/easy/190.%20颠倒二进制位.md)
- [268. 丢失的数字](https://github.com/PENTONCOS/leetcode/tree/main/easy/268.%20丢失的数字.md)
- [326. 3 的幂](https://github.com/PENTONCOS/leetcode/tree/main/easy/326.%203%20的幂.md)
- [7. 整数反转](https://github.com/PENTONCOS/leetcode/tree/main/easy/7.%20整数反转.md)


## 环问题

这类问题的特点就是，要循环寻找，到底怎么循环寻找，看题便知。

- [141. 环形链表](https://github.com/PENTONCOS/leetcode/tree/main/easy/141.%20环形链表.md)
- [160. 相交链表](https://github.com/PENTONCOS/leetcode/tree/main/easy/160.%20相交链表.md)
- [202. 快乐数](https://github.com/PENTONCOS/leetcode/tree/main/easy/202.%20快乐数.md)