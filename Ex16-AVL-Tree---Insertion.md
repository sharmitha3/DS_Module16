# Ex16 AVL Tree - Insertion
## DATE:
## AIM:
To write a C function to insert the elements in an AVL Tree.

## Algorithm
```
1. If the tree is empty, create a new node and return it.
2.If the value is less than the current node, insert in the left subtree.
3.If the value is greater than the current node, insert in the right subtree.
4.After insertion, update the height and check the balance factor.
5.If unbalanced, perform the appropriate rotation (LL, RR, LR, or RL) and return the balanced node. 
```
## Program:
```

Program to insert the elements in an AVL Tree
Developed by: Sharmitha V
RegisterNumber: 212223110048
/*typedef struct node
{
int data;
struct node *left,*right;
int ht;
}node;
node *insert(node *,int);
void preorder(node *);
//void inorder(node *);
int height(node *);
node *rotateright(node *);
node *rotateleft(node *);
node *RR(node *);
node *LL(node *);
node *LR(node *);
node *RL(node *);
int BF(node *);
*/ 
node * insert(node *T,int x)
{
    if(T==NULL){
        T=(node*)malloc(sizeof(node));
        T->data=x;
        T->left=NULL;
        T->right=NULL;
        T->ht=0;
    }
    else if(x>T->data){
        T->right=insert(T->right,x);
        if(BF(T)==-2){
            if(x>T->right->data){
                T=RR(T);
            }
            else{
                T=RL(T);
            }
        }
    }
    else if(x<T->data){
        T->left=insert(T->left,x);
        if(BF(T)==2){
            if(x>T->left->data){
                T=LL(T);
            }
            else{
                T=LR(T);
            }
        }
    }
    T->ht=height(T);
    return T;
}


```

## Output:

![image](https://github.com/user-attachments/assets/13a2db85-f264-4ea3-b9a3-82e341c005aa)


## Result:
Thus, the function to insert the elements in an AVL Tree is implemented successfully in C programming language.
