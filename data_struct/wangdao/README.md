```bash
g++ --version

g++ (Ubuntu 5.4.0-6ubuntu1~16.04.9) 5.4.0 20160609
Copyright (C) 2015 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
```

#### 5. 树与二叉树
+ 编译与执行
```bash
g++ -o ch05.o ch05.cpp ch05_tree/BiTree.cpp ch05_tree/exercises.cpp
./ch05.o
```
+ 二叉树遍历
```c
void visit(BiTNode *node);  // 访问节点

void PreOrder(BiTree T);    // 先序遍历
void InOrder(BiTree T);     // 中序遍历
void PostOrder(BiTree T);   // 后序遍历

void PreOrder2(BiTree T);   // 先序遍历(非递归)
void InOrder2(BiTree T);    // 中序遍历(非递归)
void PostOrder2(BiTree T);  // 后序遍历(非递归) 最难!

void LevelOrder(BiTree T);  // 层次遍历
```
+ 练习
```c
/* 练习 5.3 p149-p151 */
void InvertLevel(BiTree T);                             // 4. 二又树自下而上、从右到左的层次遍历算法。
int Btdepth(BiTree T);                                  // 5. 求二叉树的高度。
int BtdepthR(BiTree T);
                                                        /** ★★☆ */
BiTNode* BiTreePreinCreat(ElemType A[], int l1, int h1, // 6. 根据先序遍历序列和中序遍历序列建立二叉链表 (二叉树中各结点的值互不相同)
                          ElemType B[], int l2, int h2);

bool IsComplete(BiTree T);                              // 7. 判别二叉树是否为完全二叉树。
int DsonNodes (BiTree T);                               // 8. 计算一棵给定二叉树的所有双分支结点个数。
int DsonNodes1 (BiTree T);
void swap(BiTree T);                                    // 9. 交换二叉树中所有结点的左、右子树。
void swap1(BiTree T);
ElemType PreNode(BiTree T, int k);                      // 10. 求先序遍历序列中第 k (1<= k <= 二又树中结点个数)个结点的值。
void SearchDeleteXTree(BiTree T, ElemType x);           // 11. 对于树中每个元素值为 x 的结点，删去以它为根的子树，并释放相应的空间。

                                                        /** ★★☆ */
void Search (BiTree T , ElemType x);                    // 12. 在二叉树中查找值为 x 的结点，打印值为 x 的结点的所有祖先
bool SearchR (BiTree T , ElemType x);
                                                        /** ★★★ */
BiTree Ancestor(BiTree ROOT, BiTNode *p, BiTNode *q);   // 13. 找到 p 和 q的最近公共祖先结点 r。
BiTree AncestorR(BiTree T, BiTNode *p, BiTNode *q);
int BTWidth(BiTree T);                                  // 14. 求非空二又树 b 的宽度(即具有结点数最多的那一层的结点个数)。
void PreToPost(ElemType pre[],int l1, int h1,           // 15. 满二叉树已知其先序序列为 pre，求后序序列 post。
               ElemType post[],int l2,int h2);
BiTNode* LeafToLinikedList(BiTNode* T);                 // 16. 二叉树的叶结点按从左到右的顺序连成一个单链表
bool Similar(BiTree T1, BiTree T2);                     // 17. 判断两棵二叉树是否相似
BiTree InPostPre(BiTree t , BiTree p);                  // 18. 写出在中序线索二叉树里查找指定结点在后序的前驱结点的算法 。
int wpl(BiTree T);                                      // 19. 二又树的带权路径长度

                                                        /** ★★☆ */
void BtreeToExp(BiTree T, int depth);                   // 20. 将给定的表达式树(二叉树)转换为等价的中缀表达式并输出。
```

#### 参考
[1][C++之函数/结构体/类 模板](https://zhuanlan.zhihu.com/p/37669989)