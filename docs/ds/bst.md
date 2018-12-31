## 二叉搜索树简介

二叉搜索树是一种二叉树的树形数据结构，其定义如下：

1.  空树是二叉搜索树。

2.  若二叉搜索树的左子树不为空，则其左子树上所有点的附加权值均小于其根节点的值。

3.  若二叉搜索树的右子树不为空，则其右子树上所有点的附加权值均大于其根节点的值。

4.  二叉搜索树的左右子树均为二叉搜索树。

二叉搜索树上的基本操作所花费的时间与这棵树的高度成正比。对于一个有 $n$ 个结点的二叉搜索树中，这些操作的最优时间复杂度为 $O(\log_2 n)$ ，最坏为 $O(n)$ 。随机构造这样一棵二叉搜索树的期望高度为 $O(\log_2 n)$ 。

## 基本操作

由二叉搜索树的递归定义可得，二叉搜索树的中序遍历权值的序列为非降的序列。

遍历一棵二叉搜索树的代码如下：

```cpp
void print(int o)  //遍历以 o 为根节点的二叉搜索树
{
  if (!o) return;          //遇到空树，返回
  print(lc[o]);            //递归遍历左子树
  printf("%d\n", val[o]);  //输出根节点信息
  print(rc[o]);            //递归遍历右子树
}
```