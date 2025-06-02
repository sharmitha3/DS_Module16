# Ex17 AVL Tree – Rotation
## DATE:
## AIM:
To write a C function to perform right rotation in an AVL Tree.

## Algorithm
1. Let y = x->left (left child becomes new root).
2. Assign x->left = y->right (detach y’s right and attach it to x’s left).
3. Assign y->right = x (move x under y).
4. Update heights of x and y.
5. Return y (new root of the rotated subtree).
 

## Program:
```

Program to perform right rotation in AVL Tree
Developed by: Sharmitha V
RegisterNumber: 212223110048
/*
typedef struct node
{
int data;
struct node *left,*right;
int ht;
}node;
node *insert(node *,int);
//node *Delete(node *,int);
void preorder(node *);
//void inorder(node *);
int height( node *);
node *rotateright(node *);
node *rotateleft(node *);
node *RR(node *);
node *LL(node *);
node *LR(node *);
node *RL(node *);
*/
node * rotateright(node *x)
{
    node *y=x->left;
    x->left=y->right;
    y->right=x;
    x->ht=height(x);
    y->ht=height(y);
    return y;
}

```

## Output:

![image](https://github.com/user-attachments/assets/10011794-8b71-4c86-ac2b-a64d806c1044)


## Result:
Thus, the function to perform right rotation in an AVL Tree is implemented successfully.
