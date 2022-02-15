#include <limits.h>
#include <stdio.h>
#include <stdlib.h>
// A tree node
Struct Node {
    Int data;
    Struct Node *left, *right;
};
// A utility function to create a new node
Struct Node* newNode(int data)
{
    Struct Node* node
        = (struct Node*)malloc(sizeof(struct Node));
    Node->data = data;
    Node->left = node->right = NULL;
    Return (node);
}
// Returns maximum value in a given Binary Tree
Int findMax(struct Node* root)
{
    // Base case
    If (root == NULL)
        Return INT_MIN;
    // Return maximum of 3 values:
    // 1) Root’s data 2) Max in Left Subtree
    // 3) Max in right subtree
    Int res = root->data;
    Int lres = findMax(root->left);
    Int rres = findMax(root->right);
    If (lres > res)
        Res = lres;
    If (rres > res)
        Res = rres;
    Return res;
}
// Driver code
Int main(void)
{
    Struct Node* NewRoot = NULL;
    Struct Node* root = newNode(2);
    Root->left = newNode(7);
    Root->right = newNode(5);
    Root->left->right = newNode(6);
    Root->left->right->left = newNode(1);
    Root->left->right->right = newNode(11);
    Root->right->right = newNode(9);
    Root->right->right->left = newNode(4);
    // Function call
    Printf(“Maximum element is %d \n”, findMax(root));
    Return 0
