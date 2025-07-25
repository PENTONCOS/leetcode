
## 哈希表

`哈希表`拥有记数的功能，如果题目中包含字眼`至多xx次`， `至少xx次`,`唯一`等等字眼，可以联想到用哈希表来解决。

### 哈希表 + 计数类型
- [387. 字符串中的第一个唯一字符](https://github.com/PENTONCOS/leetcode/tree/main/easy/387.%20字符串中的第一个唯一字符.md)
- [242. 有效的字母异位词](https://github.com/PENTONCOS/leetcode/tree/main/easy/242.%20有效的字母异位词.md)
- [169. 多数元素](https://github.com/PENTONCOS/leetcode/tree/main/easy/169.%20多数元素.md)
- [136. 只出现一次的数字](https://github.com/PENTONCOS/leetcode/tree/main/easy/136.%20只出现一次的数字.md)
- [36. 有效的数独](https://github.com/PENTONCOS/leetcode/tree/main/medium/36.%20有效的数独.md)
- [187. 重复的DNA序列](https://github.com/PENTONCOS/leetcode/tree/main/medium/187.%20重复的DNA序列.md)
- [219. 存在重复元素 II](https://github.com/PENTONCOS/leetcode/tree/main/easy/219.%20存在重复元素%20II.md)
- [1436. 旅行终点站](https://github.com/PENTONCOS/leetcode/tree/main/easy/1436.%20旅行终点站.md)
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
- [49. 字母异位词分组](https://github.com/PENTONCOS/leetcode/tree/main/medium/49.%20字母异位词分组.md)

## 找规律
- [13. 罗马数字转整数](https://github.com/PENTONCOS/leetcode/tree/main/easy/13.%20罗马数字转整数.md)
- [14. 最长公共前缀](https://github.com/PENTONCOS/leetcode/tree/main/easy/14.%20最长公共前缀.md)
- [21. 合并两个有序链表](https://github.com/PENTONCOS/leetcode/tree/main/easy/21.%20合并两个有序链表.md)
- [28. 实现 strStr()](https://github.com/PENTONCOS/leetcode/tree/main/easy/28.%20实现%20strStr().md)
- [118. 杨辉三角](https://github.com/PENTONCOS/leetcode/tree/main/easy/118.%20杨辉三角.md)
- [122. 买卖股票的最佳时机 II](https://github.com/PENTONCOS/leetcode/tree/main/medium/122.%20买卖股票的最佳时机%20II.md)
- [206. 反转链表](https://github.com/PENTONCOS/leetcode/tree/main/easy/206.%20反转链表.md) 这个题必须掌握牢实，是解很多链接表题的基础的基础。
- [38. 外观数列](https://github.com/PENTONCOS/leetcode/tree/main/medium/38.%20外观数列.md)
- [48. 旋转图像](https://github.com/PENTONCOS/leetcode/tree/main/medium/48.%20旋转图像.md) 转置 + 水平翻转

## 双指针
双指针是解数组类型题最常见解法

1. 比如有头尾分别有指针，然后依次向中间靠拢的双指针，
2. 还有一种是快慢是指针，两个指针都是从左边开始，一个走的快，一个走得慢

- [26. 删除有序数组中的重复项](https://github.com/PENTONCOS/leetcode/tree/main/easy/26.%20删除有序数组中的重复项.md)
- [88. 合并两个有序数组](https://github.com/PENTONCOS/leetcode/tree/main/easy/88.%20合并两个有序数组.md)
- [125. 验证回文串](https://github.com/PENTONCOS/leetcode/tree/main/easy/125.%20验证回文串.md)
- [234. 回文链表](https://github.com/PENTONCOS/leetcode/tree/main/easy/234.%20回文链表.md) 经典题：考察快慢指针来解决找寻链表中点和链表翻转问题
- [237. 删除链表中的节点](https://github.com/PENTONCOS/leetcode/tree/main/easy/237.%20删除链表中的节点.md)
- [283. 移动零](https://github.com/PENTONCOS/leetcode/tree/main/easy/283.%20移动零.md)
- [344. 反转字符串](https://github.com/PENTONCOS/leetcode/tree/main/easy/344.%20反转字符串.md)
- [350. 两个数组的交集II](https://github.com/PENTONCOS/leetcode/tree/main/easy/350.%20两个数组的交集II.md)
- [19. 删除链表的倒数第 N 个结点](https://github.com/PENTONCOS/leetcode/tree/main/medium/19.%20删除链表的倒数第%20N%20个结点.md) 快慢指针距离：通过保持 n 个节点的距离，确保慢指针能准确定位到要删除节点的前一个位置
- [15. 三数之和](https://github.com/PENTONCOS/leetcode/tree/main/medium/15.%20三数之和.md)
- [658. 找到 K 个最接近的元素](https://github.com/PENTONCOS/leetcode/tree/main/medium/658.%20找到%20K%20个最接近的元素.md)


## 二叉树（DFS）
### 完全二叉树
在一颗二叉树中，若除最后一层外的其余层都是满的，并且最后一层要么是满的，要么在右边缺少连续若干节点，则此二叉树为完全二叉树（Complete Binary Tree）

以下都是完全二叉树：
![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/80f84d9e6d8e45a4b6be7fe3ab9a440d~tplv-k3u1fbpfcp-zoom-in-crop-mark:4536:0:0:0.awebp)

### 二叉堆
二叉堆（binary heap）是一种特殊的堆，二叉堆是完全二叉树或者是近似完全二叉树。

二叉堆满足堆特性：父节点的键值总是保持固定的序关系于任何一个子节点的键值，且每个节点的左子树和右子树都是一个二叉堆。

当父节点的键值总是大于或等于任何一个子节点的键值时为“最大堆”（max heap）。

当父节点的键值总是小于或等于任何一个子节点的键值时为“最小堆”（min heap）。
![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/de9b9f79b62b4e37bfb90e0691bd195f~tplv-k3u1fbpfcp-zoom-in-crop-mark:4536:0:0:0.awebp)
### 二叉树 前中后遍历 套路详解
前序遍历题目如下：

root节点是A节点（下图的A节点），然后让你按照下图数字的顺序依次打印出节点。

![](https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/9f23accef4a5402da0c898920e64a8f4~tplv-k3u1fbpfcp-zoom-in-crop-mark:3024:0:0:0.awebp)

我们可以看到这其中的规律，就是`深度优先遍历，先遍历左子树，再遍历右子树`，这里我们不用递归，因为一些大厂严格要求二叉树遍历不用递归，递归太简单了。

重点思路就是：`深度优先遍历，先遍历左子树，再遍历右子树`，

所以，我们需要一套如何遍历一颗二叉树，并且是先左子树，再右子树的通用模板，如下
```js
var Traversal = function(root) {
  const res = [];
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
但是下面这个 `[1,2,2,null,3,null,3]` 则不是镜像对称的：
```
    1
   / \
  2   2
   \   \
   3    3

```
**思路：**

递归解决：

- 判断两个指针当前节点值是否相等
- 判断 A 的右子树与 B 的左子树是否对称
- 判断 A 的左子树与 B 的右子树是否对称
```js 递归
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

**思路一：深度优先搜索（DFS）递归实现**
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
**思路二：深度优先搜索（DFS）迭代版本**
```js
var maxDepth = function(root) {
  if(!root) return root;
  let ret = 1;
  let stack = [[root, 1]];
  while(stack.length){
    let [node, depth] = stack.pop();
    if(!node.left && !node.right) ret = Math.max(ret, depth);
    if(node.right) stack.push([node.right, depth+1]);
    if(node.left) stack.push([node.left, depth+1]);
  }
  return ret;
}
```

- [108. 将有序数组转化为二叉搜索树](https://github.com/PENTONCOS/leetcode/tree/main/easy/108.%20将有序数组转化为二叉搜索树.md)

## 栈

栈是一种先进后出的数据结构，所以涉及到你需要`先进后出`这个想法后，就可以使用栈。

其次栈跟递归很相似，递归也是先压栈，然后先进来的先出去，就跟函数调用栈一样。


- [20. 有效的括号](https://github.com/PENTONCOS/leetcode/tree/main/easy/20.%20有效的括号.md)
- [155. 最小栈](https://github.com/PENTONCOS/leetcode/tree/main/easy/155.%20最小栈.md)
  
## 动态规划

动态规划，一定要知道动态转移方程，有了这个，就相当于解题的钥匙。

动态转移方程：使用 dp[i] 表示以第 i 个元素结尾的最大子数组和。

```js
dp[i] = Math.max(dp[i - 1] + nums[i], nums[i])
```

- [53. 最大子数组和](https://github.com/PENTONCOS/leetcode/tree/main/easy/53.%20最大子数组和.md)
- [70. 爬楼梯](https://github.com/PENTONCOS/leetcode/tree/main/easy/70.%20爬楼梯.md)
- [121. 买卖股票的最佳时机](https://github.com/PENTONCOS/leetcode/tree/main/easy/121.%20买卖股票的最佳时机.md)
- [5. 最长回文子串](https://github.com/PENTONCOS/leetcode/tree/main/medium/5.%20最长回文子串.md)
- [198. 打家劫舍](https://github.com/PENTONCOS/leetcode/tree/main/medium/198.%20打家劫舍.md)
- [647. 回文子串](https://github.com/PENTONCOS/leetcode/tree/main/medium/647.%20回文子串.md)
- [120. 三角形最小路径和](https://github.com/PENTONCOS/leetcode/tree/main/medium/120.%20三角形最小路径和.md)
- [931. 下降路径最小和](https://github.com/PENTONCOS/leetcode/tree/main/medium/931.%20下降路径最小和.md)


## 数学问题

以下更多的是涉及数学问题，这些解法非常重要，因为在中级题里面会经常用到，**中级的两数相加都是一个模板**。

- [66. 加一](https://github.com/PENTONCOS/leetcode/tree/main/easy/66.%20加一.md) 记住这个题，这是两数字相加的套路，这次是 +1，其实就是两数相加的题（腾讯面试遇到过两数相加）

  **两数相加**的模板
  ```js
  var plusOne = function(digits) {
    let carry = 1; // 进位（因为我们确定+1，初始化进位就是1）
    for(let i = digits.length - 1; i >= 0; i--){
      let sum = 0; // 这个变量是用来每次循环计算进位和digits[i]的值的
      sum = digits[i] + carry; 
      digits[i] = sum % 10; // 模运算取个位数
      carry = (sum / 10) | 0; //  除以10是取百位数，并且｜0表示舍弃小数位
    }
    if(digits[0] === 0) digits.unshift(carry);
    return digits
  };
  ```
- [69. x的平方根](https://github.com/PENTONCOS/leetcode/tree/main/easy/69.%20x的平方根.md)
- [171. Excel 表列序号](https://github.com/PENTONCOS/leetcode/tree/main/easy/171.%20Excel%20表列序号.md)
- [172. 阶乘后的零](https://github.com/PENTONCOS/leetcode/tree/main/easy/172.%20阶乘后的零.md)
- [190. 颠倒二进制位](https://github.com/PENTONCOS/leetcode/tree/main/easy/190.%20颠倒二进制位.md)
- [268. 丢失的数字](https://github.com/PENTONCOS/leetcode/tree/main/easy/268.%20丢失的数字.md)
- [326. 3 的幂](https://github.com/PENTONCOS/leetcode/tree/main/easy/326.%203%20的幂.md)
- [7. 整数反转](https://github.com/PENTONCOS/leetcode/tree/main/easy/7.%20整数反转.md)
- [2. 两数相加](https://github.com/PENTONCOS/leetcode/tree/main/medium/2.%20两数相加.md)
- [11. 盛最多水的容器](https://github.com/PENTONCOS/leetcode/tree/main/medium/11.%20盛最多水的容器.md)


## 环问题

一般都用`快慢指针`

1. **检测是否有环**：使用快慢指针，快指针每次走两步，慢指针每次走一步
2. **找到环的入口**：当快慢指针相遇后，将慢指针重置到头部，然后两个指针都以相同速度移动
3. **返回环的入口**：当两个指针相遇时，返回相遇的节点即为环的入口
4. **相交环的位置**：使用两个指针 `tempHeadA` 和 `tempHeadB`，分别从两个链表的头部开始遍历。当其中一个指针到达链表末尾时，将其指向另一个链表的头部，继续遍历。最后返回相交节点或null


这类问题的特点就是，要循环寻找，到底怎么循环寻找，看题便知。

- [141. 环形链表](https://github.com/PENTONCOS/leetcode/tree/main/easy/141.%20环形链表.md)
  
  用**快慢指针**判断是否存在环

  ```js
  var hasCycle = function(head) {
    if (!head || !head.next) return false;
    
    let slow = head;
    let fast = head.next;
    
    while (slow !== fast) {
      if (!fast || !fast.next) return false;
      slow = slow.next;
      fast = fast.next.next;
    }
    
    return true;
  };
  ```
- [142. 环形链表 II](https://github.com/PENTONCOS/leetcode/tree/main/medium/142.%20环形链表%20II.md)
  
  找到环的入口，分为两个阶段：

  1. **检测是否有环**：使用快慢指针，快指针每次走两步，慢指针每次走一步
  2. **找到环的入口**：当快慢指针相遇后，将慢指针重置到头部，然后两个指针都以相同速度移动

- [160. 相交链表](https://github.com/PENTONCOS/leetcode/tree/main/easy/160.%20相交链表.md)
- [202. 快乐数](https://github.com/PENTONCOS/leetcode/tree/main/easy/202.%20快乐数.md)


## 二分法

- [378. 有序矩阵中第 K 小的元素](https://github.com/PENTONCOS/leetcode/tree/main/medium/378.%20有序矩阵中第%20K%20小的元素.md)
- [34. 在排序数组中查找元素的第一个和最后一个位置](https://github.com/PENTONCOS/leetcode/tree/main/medium/34.%20在排序数组中查找元素的第一个和最后一个位置.md)
- [658. 找到 K 个最接近的元素](https://github.com/PENTONCOS/leetcode/tree/main/medium/658.%20找到%20K%20个最接近的元素.md)

## 滑动窗口

数据结构：数组

关键词：连续子数组、固定的子数组长度

**模版**
```js
let right = 0
let left = 0 

while (right < s.length) {
  while('条件' && left <= right) {
    // 求值
    left++
  }
  // 求值
  right++
}
```

```js
let right = 0 // 第一个指针
let left = 0 // 第二个指针

// 初始化窗口
while(right < '窗口大小') {
  right++
}

//符合条件
while (right < s.length) {
  // 求值
  left++
  // 求值
  right++
}
```

```js
let right = 0
let left = 0 

while (right < s.length) {
  while( right - left + 1 > '窗口' && left <= right) {
    // 求值
    left++
  }
  
  // 只有符合窗口大小求值
  if (right - left + 1 === '窗口大小') {
    
  }
  // 求值
  right++
}
```

- [3. 无重复字符的最长子串](https://github.com/PENTONCOS/leetcode/tree/main/medium/3.%20无重复字符的最长子串.md)
- [209. 长度最小的子数组](https://github.com/PENTONCOS/leetcode/tree/main/medium/209.%20长度最小的子数组.md)
- [1031. 两个非重叠子数组的最大和](https://github.com/PENTONCOS/leetcode/tree/main/medium/1031.%20两个非重叠子数组的最大和.md)
- [2379. 得到 K 个黑块的最少涂色次数](https://github.com/PENTONCOS/leetcode/tree/main/easy/2379.%20得到%20K%20个黑块的最少涂色次数.md)
- [219. 存在重复元素 II](https://github.com/PENTONCOS/leetcode/tree/main/easy/219.%20存在重复元素%20II.md)
- [643. 子数组最大平均数 I](https://github.com/PENTONCOS/leetcode/tree/main/easy/643.%20子数组最大平均数%20I.md)
- [658. 找到 K 个最接近的元素](https://github.com/PENTONCOS/leetcode/tree/main/medium/658.%20找到%20K%20个最接近的元素.md)
- [567. 字符串的排列](https://github.com/PENTONCOS/leetcode/tree/main/medium/567.%20字符串的排列.md)

## 递归与回溯

关键词：组合

**模版**
```js
var output = function(candidates, target){
  function dfs (remain, current, deep){
    let res = [];
    
    if(remain === 0){
      res.push([...current]);
      return;
    }

    if(deep >= candidates.length){
      return;
    }

    if(remain - candidates[deep] >= 0){
      dfs(remain - candidates[deep], [...current, candidates[deep]] , deep + 1);
    }

    dfs(remain, [...current], deep + 1);
  }

  dfs(target, [], 0)
  return res
}
```
**去重模版一**
```js
var output = function(candidates, target){
  let res = [];
  candidates.sort((a, b) => a - b); // 排序是为了方便去重

  function dfs (remain, current, deep){
    let noReaptingIndex = deep + 1; // 下一个不重复的数的指针
    
    if(remain === 0){
      res.push([...current]);
      return;
    }

    if(deep >= candidates.length){
      return;
    }

    if(remain - candidates[deep] >= 0){
      dfs(remain - candidates[deep], [...current, candidates[deep]] , deep + 1);
    }

    // 判断是否与下一个数相等
    while (candidates[noReaptingIndex] == candidates[deep]) {
      noReaptingIndex++
    }

    dfs(remain, [...current], noReaptingIndex);
  }

  dfs(target, [], 0)
  return res
}
```
**去重模版二**
去重全排列

```js
var permute = function (nums) {
  const result = [];
  const used = new Array(nums.length).fill(false);
  
  function dfs(partialResult) {
    if (partialResult.length === nums.length) {
      result.push([...partialResult]);
      return;
    }
    
    for (let i = 0; i < nums.length; i++) {
      if (!used[i]) {
        // 回溯核心机制
        used[i] = true;        // 标记使用
        partialResult.push(nums[i]);  // 加入排列
        dfs(partialResult);    // 递归
        partialResult.pop();   // 移除元素（回溯）
        used[i] = false;       // 取消标记（回溯）
      }
    }
  }
  
  dfs([]);
  return result;
};
```

- [17. 电话号码的字母组合](https://github.com/PENTONCOS/leetcode/tree/main/medium/17.%20电话号码的字母组合.md)
- [22. 括号生成](https://github.com/PENTONCOS/leetcode/tree/main/medium/22.%20括号生成.md)
- [39. 组合总和](https://github.com/PENTONCOS/leetcode/tree/main/medium/39.%20组合总和.md)
- [40. 组合总和 II](https://github.com/PENTONCOS/leetcode/tree/main/medium/40.%20组合总和%20II.md)
- [46. 全排列](https://github.com/PENTONCOS/leetcode/tree/main/medium/46.%20全排列.md) 典型的回溯问题
- [47. 全排列 II](https://github.com/PENTONCOS/leetcode/tree/main/medium/47.%20全排列%20II.md)
- [77. 组合](https://github.com/PENTONCOS/leetcode/tree/main/medium/77.%20组合.md)
